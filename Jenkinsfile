pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "Building ..."
            }
            post{
                success{
                    emailext ( to: "berenhuang@gmail.com",
                    subject: "Build Status Email",
                    body:"Pipeline ${currentBuild.fullDisplayName} completed with status: ${currentBuild.result}"
                    //attachLog: true)
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
