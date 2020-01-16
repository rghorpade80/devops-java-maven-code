pipeline {
    agent any 
    environment {
        MAVEN_HOME = tool('Maven')
        JAVA_HOME = tool('JDK')
    }
    
    stages {

         stage('MAVEN BUILD') {
            steps {
                sh '${MAVEN_HOME}/bin/mvn -B install'
              
				}
            
			} 
		stage ('UPLOAD ARTIFACT'){
		
            steps{
					nexusArtifactUploader credentialsId: 'Nexus_admin_cred', groupId: 'com.example', nexusUrl: '18.191.29.81:8081', nexusVersion: 'nexus3', protocol: 'http', repository: 'http://18.191.29.81:8081/repository/sample_repo_hosted/', version: '2.0-SNAPSHOT'
					
            }
            
        }
			
	}

}
