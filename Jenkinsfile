node {
	stages{
		stage('1-system update'){
			'system apt update -y'
		}
		stage('2-disk free space'){
			'df -h'
		}
		stage('3-real time Linux processes'){
			'top'
		}
		stage('snapshot of running processes'){
			'ps -ef'
		}
		stage('cpu analysis'){
			'lscpu'
		}
	}
}