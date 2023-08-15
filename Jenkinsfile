pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''./mvnw sonar:sonar \\
  -Dsonar.projectKey=Petclinc \\
  -Dsonar.projectName=\'Petclinc\' \\
  -Dsonar.host.url=http://172.31.10.42:9000 \\
  -Dsonar.token=sqp_5f1ce678cb1fc1715149b492418451fa0812785b'''
      }
    }

  }
}