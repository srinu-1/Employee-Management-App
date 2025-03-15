pipeline {
    agent { label 'srinu' } 

    stages {
        stage('Clone') {
            steps {
                echo "This is cloning the code"
                git branch: 'main', url: 'https://github.com/your-username/your-repo.git'
                echo "Code cloning successful"
            }
        }

        stage('Build') {
            steps {
                echo "This is building the code"
                sh "whoami"
                sh "docker build -t employee-management ."
            }
        }

        stage('Test') {
            steps {
                echo "This is testing the code"
            }
        }

        stage('Deploy') {
            steps {
                echo "This is deploying the code"
                sh "docker run -d -p 8080:80 employee-management"
            }
        }
    }
}
