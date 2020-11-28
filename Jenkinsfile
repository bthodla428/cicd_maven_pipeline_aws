pipeline {
  stages {
    stage('build') {
      agent {
        node {
          label 'jslave1'
        }

      }
      steps {
        sh 'apt install git -y'
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
        sh 'apt install git -y'
        git 'https://github.com/bthodla428/cicd_maven_pipeline_aws.git'
        sh 'mvn test'
      }
    }

  }
}
