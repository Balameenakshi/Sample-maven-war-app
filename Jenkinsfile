pipeline {

agent { label 'master' }

	tools 
	{ 
	maven "M2_HOME"
	jdk "jdk 1.8"
	}

stages {
	stage("cloning from the git")
	{
	steps { git credentialsId: 'Maven-Jar', url: 'https://github.com/Balameenakshi/Sample-maven-war-app.git' }
	}

	stage("Build using Maven")
	{
	steps { 
	bat(/"%M2_HOME%\bin\mvn" -Dmaven.test.failure.ignore clean package/) }
	}

	stage("Results")
	{
	steps { archiveArtifacts 'target/*.war' }
	}
}

}
