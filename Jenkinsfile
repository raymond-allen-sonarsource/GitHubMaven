node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'Maven';
    withSonarQubeEnv() {
      cmd "${mvn}\bin\mvn sonar:sonar"
    }
  }
}
