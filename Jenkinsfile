pipeline{
    agent any
    environment {
        NEW_VERSION = '1.3.0'
    }
    stages{
        stage("Build"){ 
            steps{
                echo "Building a Application"
                echo "Building Version is ${NEW_VERSION}"
            }
        }
        stage("Test"){
            steps{
                echo "Tesing a Application"
                echo "Building Version is ${NEW_VERSION}"
            }
        }
        stage("Deploy"){
            steps{
                echo "Deploying a Application"
                echo "Building Version is ${NEW_VERSION}"
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
