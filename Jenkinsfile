pipeline {
      agent any
    tools { maven 'maven3' }
    stages {
        stage('Github') {
           
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'jenkins-git-token-auth', url: 'https://github.com/Devops4-1/mymaven-project.git']]])
            }
        }
        stage('build'){
          
            steps{
            
                       sh 'mvn clean package'
                }
        }
    }
}
