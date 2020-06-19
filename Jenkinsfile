pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'npm install'
            }
        }
        stage('Sonarqube') {
            steps {
                echo 'Running sonarqube..'
                sh '/opt/sonarqube/sonar-client/binsonar-scanner -Dsonar.projectKey=privacy-extension -Dsonar.sources=. -Dsonar.host.url=http://localhost:9000 -Dsonar.login=c96eb2bab4afc47ca05087331588e2c697108848'
            }
        }
    }
}
