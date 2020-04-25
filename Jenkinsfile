pipeline {
    agent any
    tools {
        maven 'M2_HOME'
}
stages {
          stage('build'){
          steps {
            echo "Build step"
            sh 'mvn clean'
            sh 'mvn install'
            sh 'mvn package'
           }
         }
          stage('test'){
          steps {
            echo "test step"
            sh 'mvn test'
           }
         }
          stage('deploy'){
          steps {
            echo "deploy war file"
            build 'firstjob'
           }
        }
     }
   }
