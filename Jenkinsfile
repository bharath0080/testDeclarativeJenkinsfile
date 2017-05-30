pipeline {
    agent any
    stages {
        stage('Download Artifacts') {
            steps {
		    script {
				env.RELEASE_SCOPE = input message: 'OK to continue?', parameters: [string(defaultValue: 'Dev', description: '', name: 'Environment'), string(defaultValue: 'CSP', description: '', name: 'Component'), string(defaultValue: '1.0', description: '', name: 'Version')]
					echo "${env.RELEASE_SCOPE}"
					echo "${env.RELEASE_SCOPE.Environment}"
		    }
					                    
                }
                
            
        }
        stage('Deploy') {
            steps {
                echo 'Hello, JDK'
                sh 'java -version'
            }
        }
		
		}
}
