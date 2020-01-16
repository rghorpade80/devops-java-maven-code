pipeline {
    agent any 
    environment {
        MAVEN_HOME = tool('Maven')
        JAVA_HOME = tool('JDK')
    }
    
    stages {

         stage('MAVEN BUILD') {
            steps {
                sh '${MAVEN_HOME}/bin/mvn -B deploy'
              
			}
            
		} 

			
	}

}
