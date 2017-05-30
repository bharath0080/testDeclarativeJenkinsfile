pipeline {
    agent any
    stages {
        stage('Download Artifacts') {
		ws('/var/tmp/PROJ2') {
            steps {
		    script {
				def RELEASE_SCOPE = input message: 'OK to continue?', parameters: [string(defaultValue: 'Dev', description: '', name: 'Environment'), string(defaultValue: 'CSP', description: '', name: 'Component'), string(defaultValue: '1.0', description: '', name: 'Version')]
					echo "${RELEASE_SCOPE}"
			    		echo "In hereeeeeeeeeeeeeeeeeeeeeeeeeeeeee"
					echo ("ENVVVVVVV: "+RELEASE_SCOPE['Environment'])
			    		echo "Out of hereeeeeeeeeeeeeeeeeeeeeeeeeeeeee"
		    }
			git 'https://github.com/bharath0080/SampleStudentProject.git'
					                    
                }
                
            }
        }
        stage('Deploy') {
		ws('/var/tmp/PROJ1') {
                steps {
                echo 'Hello, JDK'
                sh 'java -version'
				git 'https://github.com/bharath0080/SampleStudentProject.git'
            }
        }
		}
		}
}
