pipeline{
    agent any
   
    stages{
        stage("Build"){
            steps {
                sh 'mvn clean package'
                echo "Compile the code and generate any necessary artifacts"
            }
        }
       
        stage("Code Quality Check"){
            steps{
                echo "Check the quality of the code"
            }
        }
        stage("Deploy"){
            steps{
                echo "Deployment the application  started and completed successfully"
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
                echo "Deployment to started and completed successfully"
            }
        }
    }   
}
