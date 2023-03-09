node {
  stage('SCM') {
    checkout scm
  }
   stage('SonarQube Analysis') {
     environment {
       Sonarqube = tool 'sonar-scanner'
     withSonarQubeEnv() {
       sh" ${sonarqube}}/bin/sonar-scanner \
          -Dsonar.projectKey=Jenkins \
          -Dsonar.sources=. "
      }
    }
  }
}
