node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    withSonarQubeEnv(installationName: 'sonarqube') {
      sh 'sonar:sonar'
    }
  }
}
