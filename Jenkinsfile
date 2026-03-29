pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Tumcha code GitHub varun pull karne
                checkout scm
            }
        }

        stage('Build & Test') {
            steps {
                echo 'Checking if index.html exists...'
                // Linux command vaprun file check karne
                sh 'ls -l index.html'
                echo 'Build Successful!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to Web Server Environment...'
                // Ithe tumhi tumche deployment logic lihu shakta
                // For example: /tmp folder madhe copy karne
                sh 'cp index.html /tmp/yathaarth_talk_index.html'
                echo 'Deployment Complete!'
            }
        }
    }

    post {
        success {
            echo 'Hooray! Pipeline Successfully Run Zali!'
        }
        failure {
            echo 'Oops! Kahi tari chukle aahe, logs check kara.'
        }
    }
}