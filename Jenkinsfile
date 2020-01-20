pipeline {
  agent {
    docker {
      image "ruby"
    }
  }
  stages {
    stages("Teste") {
      steps {
        sh "docker pull ruby"
      }
    }

    stage("Build") {
      steps {
        sh "bundle install"
      }
    }

    stage("Tests") {
      steps {
        sh "bundle exec cucumber -p ci"
      }
    }
  }
}
