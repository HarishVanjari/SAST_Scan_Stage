pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=devsecops-sast-stage -Dsonar.organization=devsecops-sast-stage -Dsonar.exclusions=**/*.css,**/*.js -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=d3a96491130621cc1445622ec43542b0142dbabf'
			}
        } 
  }
}
