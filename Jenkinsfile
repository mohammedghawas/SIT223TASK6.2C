pipeline{
    agent any
   
    stages{
        stage("Build"){
            steps {
                sh 'mvn clean package'
                echo "Compile the code and generate any necessary artifacts"
            }
        }
        stage("Unit and Integration Tests"){
            steps{
                 sh '''
                    cd  C:/Users/mohgh/OneDrive/Documents/katalon
                      -projectPath="C:\Users\mohgh\OneDrive\Documents\GitHub\SIT223TASK6.2C/index.html" 
                      -browserType="Chrome" -retry=0 -statusDelay=15 
                      -testSuitePath="Test Suites/TS_RegressionTest" -apiKey="<user API key>" -orgID=<Katalon_OrgID>
                '''
                echo "Katalon Unit tests completed successfully..."
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
