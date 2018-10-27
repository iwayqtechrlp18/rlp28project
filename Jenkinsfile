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
