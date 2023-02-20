pipeline { 
	agent { docker { image 'maven:latest' } } 
	
	stages{

		stage('Build'){
			steps{
				sh 'mvn clean install'
			}
			post{
				success{
					echo 'Succesful in Building'
				}
			}
		}
	}

 }
