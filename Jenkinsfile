node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner';
    withSonarQubeEnv('sonarqube') {
      sh "$C:\Sonarqube\sonarqube-9.9.0.65466/bin/sonar-scanner"
    }
  }
}
