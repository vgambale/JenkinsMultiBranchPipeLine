pipeline{
abcs = ['a', 'b', 'c']
	agent any
	stages{
		stage('Test 4: traditional for loop') {
        traditional_int_for_loop(abcs)
    }
	}
	def traditional_int_for_loop(list) {
    sh "echo Going to echo a list"
    for (int i = 0; i < list.size(); i++) {
        sh "echo Hello ${list[i]}"
    }
}
}