pipeline {
  
    agent any
    
    stages {
    
      stage("run frontend") {
      
          step {
             echo 'executing yarn...'
             nodejs('Node-14.7.0') {
                 sh 'yarn install'
            }
          }
          
      }
      
      stage("run backend") {
      
           step {
              echo 'executing gradle...'
              withGradle() {
                 sh './gradlew -v'
             }
             
          }
          
      }
      
   }
   
}
   
