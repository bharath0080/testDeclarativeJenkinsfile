pipeline {
  agent any
  stages {
    stage('Download Artifacts') {
      steps {
        parallel(
          "Download Artifacts": {
            ws(dir: '/var/tmp/PROJ2') {
              script {
                def RELEASE_SCOPE = input message: 'OK to continue?', parameters: [string(defaultValue: 'Dev', description: '', name: 'Environment'), string(defaultValue: 'CSP', description: '', name: 'Component'), string(defaultValue: '1.0', description: '', name: 'Version')]
                echo "${RELEASE_SCOPE}"
                echo "In hereeeeeeeeeeeeeeeeeeeeeeeeeeeeee"
                echo ("ENVVVVVVV: "+RELEASE_SCOPE['Environment'])
                echo "Out of hereeeeeeeeeeeeeeeeeeeeeeeeeeeeee"
              }
              
              git 'https://github.com/bharath0080/new-proj1.git'
            }
            
            
          },
          "Parallel_task": {
            sh 'echo "Parallel Task"'
            git(url: 'https://github.com/bharath0080/test.git', branch: 'master')
            
          }
        )
      }
    }
    stage('Deploy') {
      steps {
        ws(dir: '/var/tmp/PROJ1') {
          echo 'Hello, JDK'
          sh 'java -version'
          git 'https://github.com/bharath0080/SampleStudentProject.git'
        }
        
      }
    }
  }
}