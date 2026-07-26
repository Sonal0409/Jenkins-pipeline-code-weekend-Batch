// Write a pipeline script in Jenkinsfile format
// This pipeline will build a Java application using Maven, 
// compile code, review the code , covert pmd report , run tests, and build code.

pipeline {
    agent any
    tools{
        maven 'mymaven'
    }
    stages{
        stage('Clone the Repo'){
            steps{
                git 'https://github.com/Sonal0409/DevOpsCodeDemo.git'
            }
        }
        stage('Review Code'){
            steps{
                sh 'mvn pmd:pmd'  // Run PMD code analysis
                // generate PMD report - pmd.xml
            }
        }
        stage('Build Code'){
            steps{
                sh 'mvn package'  // Build the code using Maven
            }
        }

    }

}