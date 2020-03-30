pipeline{
	agent any
	stages{
		stage('CheckOut Solution'){
			steps{
				checkout([$class: 'GitSCM', branches: [[name: '*/release']],userRemoteConfigs: [[url: 'https://github.com/vgambale/JenkinsMultiBranchPipeLine.git']]])
			}
		}
		stage('Build Solution'){
			steps{
				bat "dotnet build --configuration Release"
			}
		}
	}
	def traditional_int_for_loop(list) {
		sh "echo Going to echo a list"
	    for (int i = 0; i < list.size(); i++) {
			sh "echo Hello ${list[i]}"
		}
	}
}