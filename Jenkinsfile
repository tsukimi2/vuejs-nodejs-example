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
        sh "docker container ps"
      }
    }
  }
}
