node {
  stage('SCM') {
    checkout scm
  }
   stage('SonarQube Analysis') {
     environment {
       sonarqube = tool 'sonar-scanner'
     withSonarQubeEnv('sonarqube') {
       sh" ${SCANNER_HOME}}/bin/sonar-scanner \
          -Dsonar.projectKey=Jenkins \
          -Dsonar.sources=. "
      }
    }
  }
}
