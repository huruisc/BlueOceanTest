pipeline{
	agent any
	
	tools{
		maven 'maven3.6.3'
	}
	
	triggers { 
		pollSCM('H/3 * * * *') 
	}
	
	stages{
		stage('Test'){
			steps{
				sh '/home/maven/apache-maven-3.6.3/bin/mvn clean install'
				junit 'target/surefire-reports/TEST-*.xml'
			}
		}
		
		stage('Deploy'){
			steps{
				echo "this is a deploying ...."
			}
		}
	}
}
