pipeline {
    agent any

    stages {
        stage('Install Packages') {
            steps {
                script {
                    sh 'sudo apt install -y git'
                    sh 'sudo apt install -y apache2'
                }
            }
        }

        stage('Run the App') {
            steps {
                script {
                    sh 'sudo systemctl start apache2'
                    sh 'sudo systemctl enable apache2'
                    sleep 5
                }
            }
        }

        stage('Visit /webapp route') {
            steps {
                script {
                    sh 'sudo rm -rf /var/www/html'
                    sh 'sudo rm -rf /var/www'
                    sh 'sudo git clone https://github.com/Saddamhussainilios/DemoCICD.git /var/www/html
                }
            }
        }
    }
}
