pipeline{
	agent any
	tools {
        maven "MAVEN_HOME"
        jdk "JDK"
    }
	triggers{
		pollSCM('* * * * *')
	}
	stages{
		stage('welcome'){
			steps{
					echo "Welcome Chowdary"
				}
		}
		stage('Source Code from GIT ') {  
             steps {  
                 sh 'hostname'
                git 'https://github.com/VenkatBramhasani/addtwointegers.git'
                 
				}  
        }
		stage('Compile Stage') {  
             steps {  
                 sh 'hostname'
                 //withMaven(maven : 'MAVEN_HOME')
					sh 'mvn clean compile'
				}
                 
        }
		stage('Test Stage') {  
             steps {  
                 sh 'hostname'
                 sh 'mvn test'
				}
                 
        }
		stage('Deploy Stage') {  
             steps {  
                 sh 'hostname'
                 sh 'mvn install'
				}
                 
        }
	}
    		
}

