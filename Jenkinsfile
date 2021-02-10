pipeline {
  agent any
  stages {
    stage('Git Clone') {
      steps {
        echo 'cloning'
      }
    }

    stage('Build & Test [Maven]') {
      steps {
        echo 'building'
      }
    }

    stage('Upload to Nexus') {
      steps {
        echo 'Uploading'
      }
    }

    stage('Dockerize the App') {
      steps {
        echo 'dockerizing'
      }
    }

    stage('Deploy to pre-prod') {
      steps {
        echo 'pre-prod deploying'
      }
    }

    stage('Run tests on pre-prod') {
      steps {
        echo 'testing'
      }
    }

    stage('Deploy onto Production') {
      steps {
        echo 'deploying'
      }
    }

    stage('Monitor') {
      steps {
        echo 'monitoring'
      }
    }

  }
}