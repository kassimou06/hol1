pipeline {
    agent any
	tools {
	    maven 'M2_HOME'
	}	
	stages {
        stage('hello') {
            steps {
                echo 'hello world'
            }

         }
	    stage('build') {
            steps {
                echo 'hello build'
		    sh 'mvn clean'
		    sh 'mvn install'
		    sh 'mvn package'
            }

         }
	    stage('deploy') {
            steps {
                echo 'hello deploy '
            }

         }
	    stage('test') {
            steps {
                echo 'hello test'
            }

         }

     }
}
