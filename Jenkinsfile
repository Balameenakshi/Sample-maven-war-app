pipeline {

agent { label 'master' }

	tools 
	{ 
	maven "M2_HOME"
	jdk "jdk 1.8"
	}

stages {
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
