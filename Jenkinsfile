pipeline {
    agent any

    stages {
        stage('code clone') {
            steps {
                echo "code cloning hogya repo se"
                git url: "https://github.com/urlearncloud/j-pro.git"
            }
        }
        stage('code build') {
            steps {
                echo "code build v karliye"
                sh "docker build . -t mywebappimg:latest"
            }
        }

        ///// if any error during code build :- install docker , sudo usermod -aG docker jenkins , sudo systemctl restart jenkins ( again build now )
        
        stage('code test') {
            steps {
                echo "code testing hogya"
            }
        }
        stage('code deploy') {
            steps {
                echo "deploying v hogya h container k andar"
                sh "docker run -itd -p 8000:8000 nodeappimg:latest"
            }
        }
    }
}
