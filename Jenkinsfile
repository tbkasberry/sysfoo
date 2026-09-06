pipeline {
  agent any
  
  tools{ 
    maven 'Maven 3.9.6'
  }
  
  stages{
      stage("build"){
          steps{
              echo 'compiling sysfoo app...'
              sh 'maven compile'
          }
      }
      stage("test"){
          steps{
              echo 'running tests on sysfoo app...'
              sh 'maven clean test'
          }
      }
      stage("package"){
          steps{
              echo 'packaging sysfoo app...'
              bat 'maven package -DskipTests'
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
    }
  }
}
