node {
  stage('SCM') {
    checkout scm
  }
  environment {
  echo "PINCHE PATH IS ${env.PATH}"
  echo "PINCHE2 PATH IS ${PATH}"
}
  stage('SonarQube Analysis') {
    def mvn = tool 'Maven';
    withSonarQubeEnv() {
      bat "${mvn}/bin/mvn sonar:sonar"
    }
  }
}
