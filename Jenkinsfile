pipeline{
	agent any
	stages{
		stage('1-system update'){
			steps{
				sh 'uptime'
			}
		}
		stage('2-disk free space'){
			steps{
				sh 'df -h'
			}
		}
		stage('3-volumeCheck'){
			steps{
				sh 'lsblk'
			}
		}
		stage('4-memoryCheck'){
			steps{
				sh 'free -m'
			}
		}
		
	}
}



