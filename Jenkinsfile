node {
  stage('SCM') {
    checkout scm
  }
   stage('SonarQube Analysis') {
     environment {
       sonarqube = tool 'sonar-scanner'
     withSonarQubeEnv('sonarqube') {
       sh" ${sonarqube}}/bin/sonar-scanner \
          -Dsonar.projectKey=Jenkins \
          -Dsonar.sources=. "
      }
    }
  }
}
