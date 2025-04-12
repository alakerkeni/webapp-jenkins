pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', 
                url: 'https://github.com/alakerkeni/webapp-jenkins.git'
            }
        }
    stage('Test') {
            steps {
                sh '''
                    echo "Running HTML validation..."
                    sudo apt-get install -y tidy  # Install HTML validator
                    tidy -q -e index.html        # Validate HTML (fails if errors)
                    echo "HTML is valid!"
                '''
            }
        }
        stage('Validate HTML') {
            steps {
                sh 'echo "Checking HTML file..."'
                sh 'ls -la' 
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying to a server..."'
               
            }
        }
    }
}
