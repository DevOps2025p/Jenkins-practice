pipeline {
    agent {
    
     node {

        label 'Agent-1'
     }
    }
environment { 
        Course = 'clang'
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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
                echo "Hello ${params.PERSON}"
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