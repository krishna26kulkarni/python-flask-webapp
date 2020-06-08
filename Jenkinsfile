pipeline {

  agent { label 'kubepod' }

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/krishna26kulkarni/python-flask-webapp.git', branch:'master'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "python.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
