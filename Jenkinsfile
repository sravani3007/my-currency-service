pipeline {
	//agent any
	agent { 
		docker {
			 image 'node:13.8'
			 }
			  }
	//agent { docker { image 'maven:3.8.4'}}
	stages{
		stage("Build"){
			steps{
				//sh 'node --version'
				echo "Build"
				echo "path- $PATH"
				echo "Build_number- $env.BUILD_NUMBER"
				echo "build_id- $env.BUILD_ID"
				echo "build_tag- $env.BUILD_TAG"
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
