pipeline {
      agent any
    tools { maven 'maven3' }
    options {
            buildDiscarder(logRotator(numToKeepStr: '5'))
            timeout(time: 1, unit: 'HOURS')
            timestamps()
     }
     triggers { pollSCM('* * * * *') }
    stages {
        
        stage('build'){
          
            steps{
            
                       sh 'mvn clean package'
                }
        }
    }
}
