pipeline{
	agent any
	stages{
		stage('CheckOut Solution'){
			steps{
				checkout([$class: 'GitSCM', branches: [[name: '*/master']],userRemoteConfigs: [[url: 'https://github.com/vgambale/JenkinsMultiBranchPipeLine.git']]])
			}
		}
		stage('Build Solution'){
			steps{
				bat "\"$(tool 'MSBuild')\" JenkinsMultiBranchPipeLine.sln /p:Configuration=Debug /p:Platform=\"Any CPU\" 
			}
		}
	}
}