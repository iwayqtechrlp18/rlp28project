pipeline{
	agent any
	stages{
		stage('SCM Checkout') {
			steps{

				git 'https://github.com/iwayqtechrlp18/rlp28project.git'
			}
		}
		stage('Maven Build'){

			steps{

				sh '/opt/apache-maven-3.5.4/bin/mvn package'
			}

		}
		stage('Code Quality Check') {

			steps{
				echo 'Code Quality is running'
				sh '/opt/apache-maven-3.5.4/bin/mvn sonar:sonar \
  -Dsonar.host.url=http://54.227.227.247:9000 \
  -Dsonar.login=70791df898c84e79a05a84531d1704f4dc980f34'
			}
		}
		stage('Publish Artifacts') {

			steps{

				echo 'Publishing Artifacts'
			}
		}
		stage('Deploy') {

			steps{

				echo 'Deploying to Test Server'
			}
		}
		stage('Testing') {
			steps{

				echo 'Tesging is going on'
			}


		}

		stage('Provide Apprivals') {
			steps{

				input('Please provide Approvals?')
			}


		}
		stage('Prod Deploy'){

			steps{

				echo 'Prod Deployments'
			}
		}




	}








}
