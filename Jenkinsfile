def scannerHome =  tool 'sonarqube';
pipeline {
  agent any
  stages {      
        
   stage('SonarQube analysis') {
    steps{
    
    withSonarQubeEnv('sonarqube') {
      sh "${scannerHome}/bin/sonar-scanner \
      -D sonar.login=admin \
      -D sonar.password=admin \
      -D sonar.projectKey=sonarqubetest \
      -D sonar.host.url=http://20.124.22.207/"
    }
  }
  }
    }
}

