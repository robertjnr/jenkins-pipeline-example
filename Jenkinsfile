pipeline {

agent any
  tools {
    maven 'Maven'
  }

    stages {

            stage('clean the code ')
            {
                steps{
                    bat 'mvn clean'
                }
            }

            stage('unit testing')
            {
                steps{
                    bat 'mvn test'
              }
          }
           stage('Package')
            {
                steps{
                    bat 'mvn install'
              }
           }
         stage('reports') {
           steps {
              script {
                allure([
                    includeProperties: false,
                    jdk: '',
                    properties: [],
                    reportBuildPolicy: 'ALWAYS',
                    results: [[path: 'target/allure-results']]
            ])
         }
        }
       }
      }
  }

