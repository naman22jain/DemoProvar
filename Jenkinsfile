pipeline {
    agent {
        dockerContainer true
    }
    stages {
        stage('Run Provar Tests') {
            steps {
                echo "Jenkins url is ${env.JENKINS_URL}"      
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"       
                sh "xvfb-run ant -f DemoProject/ANT/build.xml -v"
            }
        }
    }
    post {
        success {
            echo "Success: Good job!"
        }        
           
    }   
}
