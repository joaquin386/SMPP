pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
    stage('Test'){
      steps {
      parallel (
        "JUnit": { 
            sh "echo JUnit"
        },
        "DBUnit": { 
            sh "echo DBUnit"
        },
        "Jasmine": { 
            sh "echo Jasmine"
        },
      )
    }
    }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
