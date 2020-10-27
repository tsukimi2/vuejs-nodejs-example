pipeline {
  agent { label'node-docker-slave' }
  stages {
    stage("Build API") {
      steps {
        sh "cd api && npm install && cd .."
      }
    }
    stage("Build UI") {
      steps {
        sh "cd my-app && npm install && cd .."
      }
    }
    stage("Docker build") {
      steps {
        sh "docker build -t osiris65/vuejs-nodejs-example:latest ."
      }
    }
    stage("Docker login") {
      steps {
        withCredentials([[$class: 'UsernamePasswordMultiBinding', credentialsId: 'dockerhubCredential', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD']]) {
          sh "docker login --username $USERNAME --password $PASSWORD"
        }
      }
    }
  }
}
