pipeline {			
    agent any
    triggers {
        upstream(upstreamProjects: 'SuperUpstream',threshold: hudson.model.Result.SUCCESS)//UNSTABLE, FAILURE, NOT_BUILT, ABORTED
    }
    stages {			
        stage('Build') {			
            steps {			
                echo 'DEVELOP UPSTREAM executed'	
                echo  ${upstreamProject}
                     }			
        }			
   }		
}
