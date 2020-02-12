node ('win') {
  
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository
      git 'https://github.com/Josephreddykandi/hello-word-javacode.git'
      // Get the Maven tool.
      // ** NOTE: This 'M3' Maven tool must be configured
      // **       in the global configuration.           
      
   }
   }

node ('linux') {
   
   stage('Build') {
    
     sh 'mvn clean package'
     
   }
   stage('Results') {
      junit '**/target/surefire-reports/TEST-*.xml'
      archiveArtifacts '**/*.jar'
   }
}
