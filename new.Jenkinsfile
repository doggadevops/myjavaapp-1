pipeline {
   agent any

   

   environment {

    ARTIFACTORY_URL="http://172.31.32.31:8082/artifactory"
    ARTIFACTORY_ID="artifactory-1"
    ARTIFACTORY_CREDS="jfrog-creds"

   }
   stages{

    stage("Build Code"){
      steps {
         echo "Building Code"
      }
    }

  
   post {
      always {
         cleanWs()
      }
   }
}
