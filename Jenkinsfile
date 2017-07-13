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
		sh 'java -cp my-app/target/my-app-1.0-SNAPSHOT.jar com.mycompany.app.App '
      }
    }
  }
}