pipeline {
    agent any
    stages {
        stage('Download Artifacts') {
		agent { label 'test' }
		steps {
		ws('/var/tmp/PROJ2') {
            
		    script {
				def RELEASE_SCOPE = input message: 'OK to continue?', parameters: [string(defaultValue: 'Dev', description: '', name: 'Environment'), string(defaultValue: 'CSP', description: '', name: 'Component'), string(defaultValue: '1.0', description: '', name: 'Version')]
					echo "${RELEASE_SCOPE}"
			    		echo "In hereeeeeeeeeeeeeeeeeeeeeeeeeeeeee"
					echo ("ENVVVVVVV: "+RELEASE_SCOPE['Environment'])
			    		echo "Out of hereeeeeeeeeeeeeeeeeeeeeeeeeeeeee"
		    }
			git credentialsId: '371a964f-c1a8-4b8c-9140-7b45a872a093', url: 'https://github.com/bharath0080/new-proj1.git'
					                    
                }
                
            }
        }
        stage('Deploy') {
		
		steps {
		ws('/var/tmp/PROJ1') {
                
                echo 'Hello, JDK'
                sh 'java -version'
				git 'https://github.com/bharath0080/SampleStudentProject.git'
            }
        }
		}
		}
}
