pipeline {
    agent any
    stages {
      
        stage('Build') {
            steps {
                script {
                    build 'PES1UG22CS681-1'
                    sh 'g++ -o meow main/PES1UG22CS681.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './woof_this_is_wrong' // The executable is called meow but we are saying woof
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'This is deploying yay !'
            }
        }
    }

    post {
        failure {
            echo 'Bruh you made an error lol. Pipeline has failed'
        }
    }
}
