pipeline{
	agent any
	stages{
		stage('CheckOut Solution'){
			steps{
				checkout([$class: 'GitSCM', branches: [[name: '*/release/4.22']],userRemoteConfigs: [[url: 'https://github.com/vgambale/JenkinsMultiBranchPipeLine.git']]])
			}
		}
		stage('Build Solution'){
			steps{
				bat "dotnet build --configuration Release"
			}
		}
	}
}