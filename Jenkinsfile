pipeline{
    agent any
   
    stages{
        stage("Build"){
            steps {
                sh 'mvn clean package'
                echo "Compile the code and generate any necessary artifacts"
            }
        }
        stage(" Unit and Integration Tests"){
            steps{
                 sh '''
                    cd  /Users/yen.nguyen/Downloads/Katalon_Studio_Engine_MacOS-8.1.0/Katalon\\ Studio\\ Engine.app/Contents/MacOS
                    ./katalonc  -projectPath="/Users/yen.nguyen/Downloads/ci-samples-master/test.prj" -browserType="Chrome" -retry=0 -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest" -apiKey="<user API key>" -orgID=<Katalon_OrgID>
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
