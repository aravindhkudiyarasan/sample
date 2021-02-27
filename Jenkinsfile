pipeline {
    agent any
    tools {
        maven 'maven3'
    }
    
    stages{
	
	    stage('checkout'){
		    steps{
	          git 'https://github.com/aravindhkudiyarasan/sample.git'
            }
        stage('Build'){
            steps{
                 sh script: 'mvn mvn -B -DskipTests clean package'
                 archiveArtifacts artifacts: 'target/*.war', onlyIfSuccessful: true
            }
        }
	}
  }
}
