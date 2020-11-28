pipeline {
  agent {
    node {
      label 'slave1'
    }

  }
  stages {
    stage('build') {
      agent {
        node {
          label 'slave1'
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
          label 'slave2'
        }

      }
      steps {
        git 'https://github.com/bthodla428/cicd_maven_pipeline_aws.git'
        sh 'mvn test'
      }
    }

  }
}