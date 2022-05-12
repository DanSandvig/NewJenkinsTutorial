pipeline {
    agent any
    
    stages {
    
        stage('Clone git repo') {
            steps {
                git branch: 'main', url: 'https://github.com/DanSandvig/OtherNewJenkinsTutorial'
            }
        }
        
        stage('Run shell script') {
            steps {
                sh 'chmod +x myscript'
                sh './myscript'
            }
        }
        
        stage('Archive created file') {
            steps {
                archiveArtifacts artifacts: 'jenkinsresult.txt', followSymlinks: false
            }
        }
    }
}
