pipeline{
	agent any 
	stages{
		stage('version control'){
			steps{
				checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'cicd', url: 'https://github.com/tookiewill33/jenkins-parallel.git']]) 
			}
		}
		stage('parallel-build'){
			parallel{
				stage('substage-1'){
					steps{
						echo 'action'
					}
				}
				stage('subtage-2'){
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
