pipeline {
   agent any

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
}
