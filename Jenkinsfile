pipeline {
    agent any
	
	tools { 
        maven 'MAVEN_HOME'
        jdk   'jdk1.8'
    }
	
    stages {     
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "MAVEN_HOME = ${MAVEN_HOME}"
                ''' 
            }
        }        
        stage('Build') {
            steps {
             sh "sudo docker build -t cloud-batch:${GIT_BRANCH} docker/"
        	}
        }
        stage('Push') {
            steps {
             sh "sudo docker tag cloud-batch:${GIT_BRANCH} docker.registry.cscloud.com/cloud-batch:${GIT_BRANCH} "
             sh "sudo docker push docker.registry.cscloud.com/cloud-batch:${GIT_BRANCH}"
            }
        }
    }
}
