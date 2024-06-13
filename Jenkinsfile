pipeline {
    agent {
        dockerfile true
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
