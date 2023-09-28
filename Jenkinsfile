pipeline{
    agent any
    // parameters {
    //     choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
    //     booleanParam(name: 'executeTestStage', defaultValue: true, description: '')
    // }
    // environment {
    //     NEW_VERSION = '1.3.0'
    // }
    stages{
        stage("Build"){ 
            steps{
                echo "Building a Application"
                echo "Building Version is ${NEW_VERSION}"
            }
        }
        stage("Test"){
            // when {
            //     expression {
            //         params.executeTestStage
            //     }
            // }
            steps{
                echo "Tesing a Application"
             //   echo "Building Version is ${NEW_VERSION}"
            }
        }
        stage("Deploy"){
            steps{
                echo "Deploying a Application"
              //  echo "Building Version is ${params.VERSION}"
                
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
