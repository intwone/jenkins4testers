pipeline {
  agent {
    docker {
      image "ruby"
    }
  }
  stages {
    stage("Build") {
      stpeps {
        sh "docker run ruby"
      }

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
