pipeline{
  
  agent {label 'mykube'}
   
  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/KAVINKRISH-1212/maas.git', branch:'master'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "deployment.yml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }	


}
