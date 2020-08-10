// Every Jenkinsfile requires a pipeline statement to build the pipeline
pipeline {
  // agent keyword limits what agents can execute the pipeline as needed.
  agent any
  
  // define the stages of the pipeline
  stages {
  
    // Create the build stage
    stage ('Build') {
    
      // Define the steps within this stage
      steps {
      
        // Execute the gradle build
        echo 'Running build automation'
        sh './gradlew build --no-daemon'
        
        // Create a zip file for the final deliverable
        archiveArtifacts artifacts: 'dist/trainSchedule.zip'
      }
    }
  }
}
