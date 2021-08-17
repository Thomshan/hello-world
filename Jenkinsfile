pipeline {
  agent {
      docker{
        image 'docker.io/thomshan97/sonar_scanner'
        args '--rm -e SONAR_HOST_URL="http://10.91.11.159:9000" -e SONAR_LOGIN="5294ef30766a00c7f2588974df733ceb28cc887e" -v ${env.WORKSPACE}:/usr/src -Dsonar.projectKey=myproject'
      }
  }
  stages {
    stage('Git Clone') {
      steps {
        git checkout;
      }
    }

    stage('Static Analysis') {
      steps {
        script{
            def scannerHome = tool 'SonarScanner'
            withSonarQubeEnv('My SonarQube Server') {
            sh "${scannerHome}/bin/sonar-scanner"
        }
    }
    }
    }
  }
}
