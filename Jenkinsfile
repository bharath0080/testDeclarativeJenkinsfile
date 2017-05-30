pipeline {
    agent any
    stages {
        stage('Example Build') {
            steps {
                choice = new ChoiceParameterDefinition('Param name', ['option1', 'option2'] as String[], 'Description')
                input message: 'Select one', parameters: [choice]
                echo 'Hello, Maven'
                sh 'mvn --version'
            }
        }
        stage('Example Test') {
            steps {
                echo 'Hello, JDK'
                sh 'java -version'
            }
        }
    }
}
