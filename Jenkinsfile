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
      }
  }

