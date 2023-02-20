pipeline { 

	agent { docker { image 'maven:latest' } } 
	
	stages{
stage('Initialize'){
        def dockerHome = tool 'Docker-Image'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
    }
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
