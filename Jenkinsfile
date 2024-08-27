pipeline {
    agent any

    stages {
        stage('Login and Deploy') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'omar-id', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
                    sh '''
                        echo "Logging in with user: $USERNAME"
                        echo $PASSWORD | docker login -u "$USERNAME" --password-stdin
                    '''
                }
            }
        }
