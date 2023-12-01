pipeline {
    
    agent any 
    
    stages {
        
        stage('Checkout'){
           steps {
		   script {
                    // Replace 'https://github.com/your-username/your-repo.git' with your Git repository URL
                    checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/sagilipavan94/pavan1994.git']]])
                }
           }
        }

        stage('Build and Run Java'){
            steps{
                script{
			def jdkHome = tool 'openjdk-11-jre'
                        sh "${jdkHome}/bin/javac HelloWorld.java"
                        sh "${jdkHome}/bin/java HelloWorld"
                }
            }
        }
    }
}
