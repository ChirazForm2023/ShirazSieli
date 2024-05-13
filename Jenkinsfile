pipeline{
    agent any
    stages {
        stage ("CONTINUOUS DOWNLOAD"){
            steps{
                git branch: 'main', url: 'https://github.com/ChirazForm2023/Sieli-code.git'
            }
        }
        stage("Unit Test") {
            steps {
                sh 'mvn test'
            }
        }

        stage("Integretion Test") {
            steps {
                sh 'mvn verify -DskipUnitTests'
            }
        }

        stage("Continuous Build") {
            steps {
                sh 'mvn clean install'
            }
        }
        
    }
}