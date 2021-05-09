pipeline {
	agent any
	stages {
		stage ('Build') {
			steps {
					echo "Building the code!!";
					bat 'Build.bat'
					}
				}

		stage ('Unit-test') {
			steps {
					echo "Testing the code!!";
				bat 'Unit.bat'
					}
				}
				
		stage ('Quality-gate') {
			steps {
					echo "Verifying quality gates!!";
					bat 'Quality.bat'
					}
				}
		
		stage ('Deploy') {
			steps {
					echo "Deploying the code!!";
					bat 'Deploy.bat'
					}
				}
			}
		post {
			always {
				echo 'This will always run'
				}
			success {
				echo 'This will run only if successful'
				}
			failure {
				echo 'This will run only if failed'
				}
			unstable {
				echo 'This will run only if the run was marked as unstable'
				}
			changed {
				echo 'This will run only if the state of the pipeline has changed'
				echo 'For example, if the pipeline was previously failing but now successful'
				}
			}
		}
