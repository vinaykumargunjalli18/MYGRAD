pipeline{
	agent any
	tools{
		gradle 'Gradle'
		}
	stages{
		stage('Checkout'){
			steps{
				git branch:'main',url:'https://github.com/vinaykumargunjalli18/MYGRAD'
				}
			}
		stage('Build'){
			steps{
				sh 'gradle build'
				}
			}
		stage('Test'){
			steps{
				sh 'gradle test'
				}
			}
		stage('run'){
			steps{
				sh 'gradle run'
				}
			}
		}
	post{
		success{
			echo 'Build and Deployment Successful'
			}
		failure{
			echo 'Build failure'
			}
		}
	}
