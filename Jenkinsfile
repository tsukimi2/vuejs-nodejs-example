pipeline {
  agent { label'node-docker-slave' }
  stages {
    stage("Build API") {
      steps {
        sh "cd api && ls -la && cd .."
      }
    }
    stage("Build UI") {
      steps {
        sh "cd my-app && ls -la"
      }
    }
  }
}
