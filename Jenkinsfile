node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner';
    withSonarQubeEnv('sonarqube') {
      sh '''
        ${JENKINS_HOME}/tools/hudson.plugins.sonar.SonarRunnerInstallation/SonarQube_Scanner/bin/sonar-scanner \
                   -Dsonar.host.url=http://192.168.68.103:9000 \
                   -Dsonar.login=squ_fefb0ad683c41a8170385110d40b3839f3f24c13 \
                   -Dsonar.projectName=Jenkins
      '''
    }
  }
}
