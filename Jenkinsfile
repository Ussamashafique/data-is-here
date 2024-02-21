pipeline {
	agent {
		docker {
			image 'maven:3.8.1'
		} 
	}
  stages {
		stage('Build') {
			steps {
				dir('hello-world-java'){
					sh 'mvn -B -DskipTests clean package'
				}
			} 
		}
    stage('Test') {
			steps {
				dir('hello-world-java'){
					sh 'java -jar target/hello-world-1.jar'
				}
			} 
		}
	}
}
