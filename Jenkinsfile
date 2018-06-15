pipeline {
  agent any
  stages {
    stage('Fetch') {
      steps {
        echo 'fetching the code...'
      }
    }
    stage('Code Compilation') {
      parallel {
        stage('Compile') {
          steps {
            echo 'Compiling the code'
          }
        }
        stage('') {
          steps {
            bat 'javac HelloDemo.java'
          }
        }
      }
    }
    stage('Running the code') {
      parallel {
        stage('Execute') {
          steps {
            echo 'Executing....'
          }
        }
        stage('') {
          steps {
            bat 'java HelloDemo'
          }
        }
      }
    }
    stage('Reports') {
      steps {
        echo 'Publishing Reports'
      }
    }
  }
}