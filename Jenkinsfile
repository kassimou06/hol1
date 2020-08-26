pipeline {
    agent any
	tools {
	    maven 'M2_HOME'
	}	
	stages {
		
	    stage('build') {
            steps {
                echo 'hello build'
		    sh 'mvn clean'
		    sh 'mvn install'
		    sh 'mvn package'
            }

         }
	    stagte('test') {
            steps {
                sh 'mvn test'
            }

         }
	    stage('build and publish image') {
            steps {
	      script{  
		checkout scm
	        docker.WithRegistry('', 'DockerRegistryID') {
		def customImage = docker .build("03150627/hol-pipeline:${env.BUILD_ID}")
		customImage.push()	
            }

         }

     }
} 
		
	}
}	
	
