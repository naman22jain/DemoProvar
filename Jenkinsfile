pipeline {
    agent any
    stages {
        stage('Run Provar Tests') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"       
                sh "ant -f ANT/build.xml -v"
            }
        }
    }
    post {
        success {
            echo "Success: Good job!"
        }        
    }   
}
