node {
    stage('SCM') {
       checkout scm
       }
    stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner';
        withSonarQubeEnv(installationName: 'sonarqube') {
            sh '.mvnw clean org.sonarsource.scanner.maven:sonar-maven-plugin:3.9.0.2155:sonar'
            -Dsonar.analysis.mode=
                }
    }
}
