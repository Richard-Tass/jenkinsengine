pipeline{
	agent{
		label 'slave1'
	}
	stages{
		stage('1-clone'){
			steps{
				sh 'cat /etc/passwd'
			}
		}
		stage('2-freeMemoryG'){
			agent{
				label 'slave2'
			}
			steps{
				sh 'free -g'
			}
		}
		stage('3-memorycheckM'){
			agent{
				label 'slave3'
			}
			steps{
				sh 'free -m'
			}
		}
		stage('4-freeDiskspace'){
			agent{
				label 'slave4'
			}
			steps{
				sh 'df -h'
			}
		}
		stage('5-done'){
			agent{
				label 'slave1'
			}
			steps{
				sh 'echo "we are done"'
			}
		}
	}
}

