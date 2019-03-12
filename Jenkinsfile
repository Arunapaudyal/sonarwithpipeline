node {
  stage('SCM') {
    git 'https://github.com/csenapati12/maven-samples.git'
  }
  stage('build & SonarQube Scan') {
    withSonarQubeEnv('sonar') {
      sh '''
      
      mvn clean package sonar:sonar
      '''
    } 
  }
}
