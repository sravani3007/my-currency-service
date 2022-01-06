pipeline {
	agent any
	//agent { docker { image 'maven:3.8.4'}}
	stages{
		stage("Build"){
			steps{
				//sh 'node --version'
				echo "Build"
			}
		}

		stage("Test"){
			steps{
				echo "Test"
			}
		}

		stage("Integration Test"){
			steps{
				echo "Integration Test"
			}
		}
	}
	post{
		always{
			echo'im always success'
		}
		success{
			echo'hurre, i ran successfully'
		}
		failure{
			echo'sorry, code got failed'
		}
		changed{
			echo'oh... the buil status changed'
		}
	}
}
