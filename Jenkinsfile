pipeline {
  agent any
  stages {    
    stage('data_creation') {
      steps {
        echo 'Create data'
        sh 'python3 data_creation.py'
      }
    }

    stage('data_preprocessing') {
      steps {
        echo 'data preprocessing'
        sh 'python3 model_preprocessing.py'
      }
    }
    
    stage('data_preparation') {
      steps {
        echo 'model_preparation'
        sh 'python3 model_preparation.py'
      }
    }
    
    stage('model_testing') {
      steps {
        sh 'python3 model_testing.py'
        echo 'model_testing'
      }
    }
  }
}
