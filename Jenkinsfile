pipeline {
	agent any 
    tools
    {
        maven "maven"
    }
	stages{
		stage("Git Integration with Jenkins"){
            steps{
                git branch: 'main', url: "https://github.com/Devops9AM/Rigstration-Form.git"
        }
           	}
        stage("Cleaning the Artifact by Maven"){
            steps{
                sh 'mvn clean'
            }
        }
        stage ("Testing the code"){
            steps{
                sh 'mvn test'
            }
        }
        stage ("Building the Artifact by Maven"){
            steps{
                sh 'mvn package'
            }
        }
        stage("Deploy Artifact into Nexus Server"){
            steps{
                sh 'mvn deploy'
                
            }
            }
        }
}
