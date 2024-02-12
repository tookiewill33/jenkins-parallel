pipeline{
	agent any 
	stages{
		stage('version control'){
			steps{
				git checkout 
			}
		}
		stage('parallel-build'){
			parallel{
				stage('substage-1'){
					steps{
						echo 'action'
					}
				}
				stage('subtage-1'){
					steps{
						echo 'action 2'
					}
				}
			}
		}
		stage('code-build'){
			steps{
				sh 'cat /etc/passwd'
			}
		}
	}
}