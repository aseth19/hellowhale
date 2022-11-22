pipeline {

  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/aseth19/hellowhale.git', branch:'master'
      }
    }
    
      stage("Build image") {
            steps {
                script {
                    myapp = docker.build("anmolseth007/hellowhale:${env.BUILD_ID}")
                }
            }
        }
  }

}
