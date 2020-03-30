abcs = ['a', 'b', 'c']

node('master') {
    stage('Test 1: loop of echo statements') {
        echo_all(abcs)
    }   
    stage('Test 4: traditional for loop') {
        traditional_int_for_loop(abcs)
    }
}

@NonCPS // has to be NonCPS or the build breaks on the call to .each
def echo_all(list) {
    list.each { item ->
        echo "Hello ${item}"
    }
}
// outputs only the "Going to echo a list" bit

//No NonCPS required
def traditional_int_for_loop(list) {
    sh "echo Going to echo a list"
    for (int i = 0; i < list.size(); i++) {
        sh "echo Hello ${list[i]}"
    }
}
// echoes everything as expected
