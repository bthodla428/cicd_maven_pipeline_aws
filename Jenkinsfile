pipeline {
  agent any
  
  tools { 
        maven 'M3' 
  }
  
  stages {
    stage('build') {
      agent {
        node {
          label 'jslave1'
        }

      }
      steps {
        git 'https://github.com/bthodla428/cicd_maven_pipeline_aws.git'
        sh 'mvn compile'
      }
    }

    stage('test') {
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
