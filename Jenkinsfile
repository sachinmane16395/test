pipeline
{
	options {
				buildDiscarder(logRotator(numToKeepStr: '5', artifactNumToKeepStr: '5'))
		    }
  agent any
  tools
	{
		maven 'Maven3.8'
	}
	stages
	{
		stage('code comiplation')
		{
						steps
						{
						echo 'code comiplation started'
						sh 'mvn clean compile'
						echo 'code compilation finished'
						}
		}
		stage('code packaging')
		{
						steps
						{
						echo 'code packaging started'
						sh 'mvn clean package'
						echo 'code packaging finished'
						}
		}
		stage('create docker image')
		{
						steps
						{
						echo 'create docker image'
					    }
		}
		stage('docker image tag')
		{
						steps
						{
						echo 'docker image tag'
					    }
		}
		stage('push docker image to docker hub')
		{
						steps
						{
						echo 'push docker image to docker hub'
					    }
		}
		stage('push docker image to AWS ECR')
		{
						steps
						{
						echo 'push docker image to AWS ECR'
					    }
		}
		stage('push docker image to nexus')
		{
						steps
						{
						echo 'push docker image to nexu'
					    }
		}
		stage('deploy apps to k8')
		{
						steps
						{
						echo 'deploy app to k8'
					    }
		}
	}

}