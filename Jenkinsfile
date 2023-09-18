pipeline{
    agent any
    stages{
        // stage("Check Out"){
        //     steps{
        //         git url: "https://github.com/Ranjith-Qprofiles/DevOpsClassCodes.git"
        //     }
        // }
        stage("Code-Compile"){
            steps{
                sh 'mvn compile'
            }
        }
        stage("Code-Test"){
            steps{
                sh 'mvn test'
            }
        }
        stage("Code-QA-PMD"){
            steps{
                sh 'mvn pmd:pmd'
                recordIssues(tools: [pmdParser()])
            }   
        }
        stage("Code-QA-CheckStyle"){
            steps{
                sh 'mvn checkstyle:checkstyle'
                recordIssues(tools: [checkStyle()])
            }
        }
        stage("Code-Package"){
            steps{
                sh 'mvn package'
            }
        }
    }
}
