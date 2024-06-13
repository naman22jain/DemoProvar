pipeline {
        
agent {
        dockerfile {
            filename 'Dockerfile'
            dir 'DemoProject' // Specify the directory containing your Dockerfile
        }
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from Git
         git 'https://github.com/naman22jain/DemoProvar.git'
            }
        }
        stage('Build') {
            steps {
                  echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                script {
                    docker.build("my-image")
            }
            
        }
        
    }
       post {
        success {
            echo "Success: Good job!"
        }        
             
    }   
}

