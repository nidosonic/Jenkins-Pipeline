pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "Building ..."
            }
            post{
                success{
                    mail to: "berenhuang@gmail.com",
                    subject: "Build Status Email",
                    body:"Pipeline ${currentBuild.fullDisplayName} completed with status: ${currentBuild.result}",
                    attachLog: true
                }

                // success {
       // echo 'Pipeline completed successfully.'
        // Send notification emails using the Email Extension plugin
       // emailext to: "berenhuang@gmail.com",
       // body: "Pipeline ${currentBuild.fullDisplayName} completed with status: ${currentBuild.result}",
        //subject: "Jenkins Pipeline: ${currentBuild.fullDisplayName}",
       // attachLog: true
    }
            }
        }
        stage("Test"){
            steps{
                echo "Testing ..."
            }
        }

        stage("Deploy"){
            steps{
                echo "Deploying ..."
            }
        }
        
        stage("Complete"){
            steps{
                echo "Completed ..."
            }
        }



        
    }

}
