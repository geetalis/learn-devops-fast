pipeline { 
	agent { docker { image 'maven:amazoncorretto' } } 
	
	stages{

		stage('Build'){
			steps{
				sh 'mvn --version'
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
