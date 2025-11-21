pipeline {
    agent {
    
     node {

        label 'Agent-1'
     }
    }
environment { 
        Course = 'clang'
    }
//build///
    stages {
        stage('Build') {
            steps {
                   sh """
                      echo "hello build"
                      env
                      """


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
//post build//
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success { 
            echo 'Hello Successfully'
        }
    }
}