pipeline {

 agent any

 stages {
    stage("Distributed Builds"){

        parallel {
            stage("Build-on-Linux"){
               steps {
                  echo "Building on Linux"
               }
            }
            stage("Build-on-Windows"){
               steps {
                  echo "Building on Windows"
               }
            }
            stage("Build-on-Andriod"){
               steps {
                  echo "Building on Andriod"
               }
            }
    
        }

    }

    stage("Code Analysis"){
        steps {
            echo "Running Code Analysis"
        }
    }

    stage("Upload Artifacts"){
        steps {
            echo "Uploading artifacts..."
        }
    }
    


 }



}
