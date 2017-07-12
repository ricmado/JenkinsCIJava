#!/usr/bin/env groovy


pipeline {
  agent any

  stages {
    stage('build') {
      steps {
        sh 'javac *.java'
        }
    }
    stage('run') {
      steps {
        sh 'java HelloWorld'
		echo env.JOB_NAME
      }
    }
  }
}