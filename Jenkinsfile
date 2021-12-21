pipeline {			
    agent any
    triggers {
        upstream(upstreamProjects: 'SuperUpstream',threshold: hudson.model.Result.SUCCESS)//UNSTABLE, FAILURE, NOT_BUILT, ABORTED
    }
    stages {			
        stage('Build') {			
            steps {			
                echo 'TRIFFER DEVELOP DOWNSTREAM '
                build job: 'dev1' , propagate: false
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                
                build job: 'dev2Multibranch/develop' , propagate: false
                echo "Pipeline currentResult: ${currentBuild.currentResult}"
                     }			
        }			
   }		
}
