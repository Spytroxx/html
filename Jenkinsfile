pipeline {
    agent any
    stages {
        stage('install httpd') {
            steps {
               sh 'sudo yum install httpd -y'
            }
        }
        stage('copy files and start') {
            steps {
                sh '''sudo systemctl start httpd
                      sudo systemctl enable httpd
                      sudo cp -rvf index.html /var/www/html
                      sudo systemctl restart httpd
              '''
            }
        }
        
}
}
