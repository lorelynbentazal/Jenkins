node {
  stage('SCM') {
    checkout scm
  }
  stages {
    stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner';
    }
     stage(Env Variables) {
      environment {
        Name = "sonarqube"
        steps {
          sh 'sonar-scanner'
        }
      }
    }
  }
}
