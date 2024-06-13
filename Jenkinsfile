pipeline {
    agent {
        dockerfile true
    }
 environment {
        // Define an absolute path for the workspace directory
        WORKSPACE_DIR = "C:/Users/naman.jain/jenkins/workspace"
    }
    stages {
        stage('Run Provar Tests') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"       
                sh "xvfb-run ant -f ANT/build.xml -v"
            }
        }
    }
    post {
        success {
            echo "Success: Good job!"
        }        
    }   
}
