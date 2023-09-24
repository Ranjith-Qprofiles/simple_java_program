pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                echo "Building a Application"
            }
        }
        stage("Test"){
            steps{
                echo "Tesing a Application"
            }
        }
        stage("Deploy"){
            steps{
                echo "Deploying a Application
            }
        }
    }
    post{
        success {
            echo "Success Build"
        }
        failure{
            echo "Failure Build"
        }
        always{
            echo "Alway send a Mail to Developers"
        }
    }
}
