pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', 
                url: 'https://github.com/alakerkeni/webapp-jenkins.git'
            }
        }

        stage('Validate HTML') {
            steps {
                sh 'echo "Checking HTML file..."'
                sh 'ls -la'  // Verify index.html exists
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying to a server..."'
                // Example: Deploy to a local Nginx container (adjust as needed)
                sh '''
                    docker cp index.html nginx-container:/usr/share/nginx/html/
                    docker exec nginx-container service nginx reload
                '''
            }
        }
    }
}
