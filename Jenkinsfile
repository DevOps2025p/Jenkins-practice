pipeline {
    agent {
     node {
#####Agent-1 is my label##########
        label 'Agent-1'
     }
    }
#####Build##########################

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}