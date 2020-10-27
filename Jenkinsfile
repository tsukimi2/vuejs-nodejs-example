pipeline {
  agent { label'node-docker-slave' }
  stages {
    stage("Build") {
      steps {
        sh "cd api; ls -la"
      }
    }
  }
}
