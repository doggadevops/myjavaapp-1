pipeline {

 agent any

 stages {
    stage("Distributed Builds"){

        parallel {
            stage("Build-on-Linux"){
               steps {
                  echo "Building on Linux"
                  //sleep time: 1, unit: 'MINUTES'
               }
            }
            stage("Build-on-Windows"){
               steps {
                  echo "Building on Windows"
                  //sleep time: 1, unit: 'MINUTES'
               }
            }
            stage("Build-on-Andriod"){
               steps {
                  echo "Building on Andriod"
                  //sleep time: 1, unit: 'MINUTES'
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
    //}
    


 }

 post{
        // always{
        //     slackSend( channel: "#jenkins-devops-batch4", token: "HLKGjEFDK61t0rqWgNPqjKJZ", color: "good", message: "Completed Job Successfully")
        // }
        failure{
            slackSend( channel: "#jenkins-devops-batch4", token: "HLKGjEFDK61t0rqWgNPqjKJZ", color: "#FF0000", message: "Job has been failed, please look into this issue.")
        }

        success{
            slackSend( channel: "#jenkins-devops-batch4", token: "HLKGjEFDK61t0rqWgNPqjKJZ", color: "good", message: "Job has been completed successfully! ")
        }
    }

}
