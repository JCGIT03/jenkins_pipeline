pipeline{
  agent any

  stages{
    stage('docker build') {
      step {
        script {
          sh "docker build -f /Dockerfile -t caosbinario/homer_page/1.0.0-${BUILD_ID} /"
        }
      }
    }
    stage('docker push') {
      steps {
        script {
          sh "docker push caosbinario/homer_page:1.0.0-${BUILD_ID}"
        }
      }
    }
  }
}
