pipeline{
	agent any
	stages{
		stage('1-repo clone'){
			steps{
				sh 'checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'e887658f-a27b-4cdd-908d-41cf6eeebe37', url: 'https://github.com/Richard-Tass/jenkinsengine.git']]])'
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
		}stage('5-securityCheck'){
            steps{
                sh 'bash -x/var/lib/jenkins/workspace/pipeline-system analysis/security.sh
'
            }
        }
		
	}
}



