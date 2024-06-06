pipeline {
        
agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from Git
                git 'https://github.com/naman22jain/DemoProvar.git'
            }
        }
        
        stage('Build') {
            steps {
                // Pass parameters to Ant build script using system properties
                bat "ant -f DemoProject/ANT/build.xml"
            }
        }
    }
}
