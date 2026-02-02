pipeline {
    agent any                          // Run on any available agent

    stages {
        stage('Checkout') {            // Stage 1: Get the code
            steps {
                echo 'Checking out code...'
            }
        }
        stage('Install') {             // Stage 2: Install dependencies
            steps {
                echo 'Installing dependencies...'
                sh 'pip install pandas numpy'   // Shell command
            }
        }
        stage('Test') {                // Stage 3: Run tests
            steps {
                echo 'Running tests...'
                sh 'python -c "import pandas; print(pandas.__version__)"'
            }
        }
        stage('Deploy') {              // Stage 4: Deploy
            steps {
                echo 'Deploying...'
                echo 'Pipeline complete!'
            }
        }
    }
}
