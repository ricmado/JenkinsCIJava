#!/usr/bin/env groovy


pipeline {
  agent any
	tools {
        maven 'MAVENAut'
        }
  stages {
    stage('build') {
      steps {
        sh 'mvn -f ./my-app/pom.xml package'
        }
    }
    stage('run') {
      steps {
		echo env.JOB_NAME
      }
    }
  }
}