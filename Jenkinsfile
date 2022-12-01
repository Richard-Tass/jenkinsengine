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
		stage('3-real time Linux processes'){
			steps{
				sh 'top'
			}
		}
		stage('4-cpu analysis'){
			steps{
				sh 'lscpu'
			}
		}
		
	}
}



