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

                sh "ant -f ${pwd()}/DemoProject/ANT/build.xml -v"
            }
            
        }
        
    }
       post {
        success {
            echo "Success: Good job!"
        }        
             
    }   
}

