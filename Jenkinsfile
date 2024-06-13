pipeline {
        
agent {
    dockerfile true
}

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from Git
         git 'https://github.com/naman22jain/DemoProvar.git'  https://github.com/naman22jain/DemoProvar.git
            }
        }
        stage('Build') {
            steps {
                 echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"       

                sh "ant -f DemoProject/ANT/build.xml"
            }
            
        }
        
    }
       post {
        success {
            echo "Success: Good job!"
        }        
             
    }   
}

