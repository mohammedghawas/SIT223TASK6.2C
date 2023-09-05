pipeline{
    agent any
    environment{
        DIRECTORY_PATH = "SIT223"
        TESTING_ENVIRONMENT = "staging.deakin.au.ac"
        PRODUCTION_ENVIRONMENT = "new.deakin.au.ac"
    }
    stages{
        stage("Build"){
            steps{
                echo "Fetch the source code from $DIRECTORY_PATH "
                echo "Compile the code and generate any necessary artifacts"
            }
        }
        stage("Test"){
            steps{
                echo "Unit tests completed successfully..."
                echo "Integration tests completed successfully.."
            }
        }
        stage("Code Quality Check"){
            steps{
                echo "Check the quality of the code"
            }
        }
        stage("Deploy"){
            steps{
                echo "Deployment the application to $TESTING_ENVIRONMENT started and completed successfully"
            }
        }
        stage("Approval"){
            steps{
                sleep 10
                echo "Approval started and completed successfully"
            }
        }
         stage("Deploy to Production"){
            steps{
                echo "Deployment to $PRODUCTION_ENVIRONMENT started and completed successfully"
            }
        }
    }   
}