// start of pipeline
pipeline {
  // where pipeline job will run
  agent {
    label "slave"
  }
  
  // start of stages : build, test, deploy ...
  stages {
    // start of stage : build
    stage('build') {
      // start of running steps inside one stage
      steps {
        // invoke command to build with maven
        bat 'mvn clean install'
      }
    }
    
        // start of deploy state
    stage('deploy') {
      // define step to run
      steps {
        //invoke command to stop tomcat service
        sh '''#!/bin/bash

                    echo "Hello from bash"
                    echo "Who I'm $SHELL"
                '''
      }
    } 

    
  } 
}

