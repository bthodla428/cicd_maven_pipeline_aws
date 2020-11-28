pipeline {
  agent any
  
  tools { 
        maven 'M3' 
  }
  
  stages {
    stage('Building Maven Project') {
      agent {
        node {
          label 'jslave1'
        }

      }
      steps {
        git 'https://github.com/bthodla428/cicd_maven_pipeline_aws.git'
        sh 'mvn install'
      }
    }

    stage('Testing Maven Project') {
      agent {
        node {
          label 'jslave2'
        }

      }
      steps {
        git 'https://github.com/bthodla428/cicd_maven_pipeline_aws.git'
        sh 'mvn test'
      }
    }

  }
}
