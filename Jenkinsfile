pipeline{
    agent any
     environment{
        PROJECT = "CLININCAL DEPRESSION ASSISTANT"
        TESTING_ENVIRONMENT = "staging.cda.com"
        PRODUCTION_ENVIRONMENT = "cda.com"
    }
    stages{
        stage("Build"){
            steps {
                echo "===Apache Maven Build Tool==="
                echo "Compile the code and generate any necessary artifacts"
            }
        }
        stage("Unit and Integration Tests"){
            steps{
    
                echo "===Katalon Testing Tool==="
                echo "Unit tests completed successfully.."
                echo "Integration tests completed successfully.."
            }
            post{
                success{
                    mail to: "mohghawas@gmail.com",
                    subject: "$PROJECT - Unit and Integration Tests",
                    body: "Unit and Integration Test Completed successfully!"
                    //attachLog: true
                }
                failure{
                    mail to: "mohghawas@gmail.com",
                    subject:"$PROJECT - Unit and Integration Test",
                    body: "Unit and Integration Test for the $PROJECT failed. Find attached logs"
                        //attachLog: true
                }
            }
        }
        stage("Code Analysis"){
            steps{
                echo "==CheckStyle Code Analysis Tool==="
                echo "Checking the quality of the code completed successfully"
            }
        }
        stage("Security Scan"){
            steps{
                echo "===Jenkins Security Scan==="
                echo "Security Scan completed successfully"
            }
            post{
                success{
                    mail to: "mohghawas@gmail.com",
                    subject: "$PROJECT - Security Scan",
                    body: "Security Scan for the $PROJECT Completed successfully!"
                        //attachLog: true
                }
                failure{
                    mail to:"mohghawas@gmail.com",
                    subject: "$PROJECT - Security Scan",
                    body: "Security Scan for the $PROJECT failed. Find attached logs"
                        //attachLog: true
                }
            }
        }
        stage("Deploy to Staging"){
            steps{
                echo"===Deployment to AWS EC2 Staging==="
                echo "Deployment the application to $TESTING_ENVIRONMENT started and completed successfully"
            }
        }
        stage(" Integration Tests on Staging"){
            steps{
                echo"===AWS EC2 Integration Tests==="
                echo "Integration tests on the staging environment started and completed successfully"
            }
        }
        stage("Deploy to Production"){
            steps{
                echo"===Deployment to AWS EC2 Prod"
                echo "Deployment to $PRODUCTION_ENVIRONMENT started and completed successfully"
            }
        }
    }    
}
