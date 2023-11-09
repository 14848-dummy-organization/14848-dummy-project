node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'Default Maven';
    withSonarQubeEnv() {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=14848-dummy-organization_14848-dummy-project_AYuzgQWqzf3uiQm7R14q -Dsonar.projectName='14848-dummy-project'"
    }
  }
}
