pipeline{
	pipeline{
		agent{
			label 'slave1'
		}
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
		stage('4-volumeCheck'){
			agent{
				label 'slave4'
			}
			steps{
				sh 'lsblk'
			}
		}
		stage('5-diskfreespace'){
			agent{
				label 'slave1'
			}
			steps{
				sh 'df -h'
			}
		}
	}


