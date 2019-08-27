pipeline {

agent { label 'master' }

stage("cloning from git")
{
steps { echo "Am cloning from git" }
}

stage("Build using Maven")
{
steps { echo "Am building using Maven" }
}

stage("Results")
{
steps { echo "This is the test stage" }
}

}
