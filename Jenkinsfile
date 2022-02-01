pipeline {
    agent any 
	stages { 
	  stage('checkout'){
    		steps{
    		    script{
	    		checkout([
        		    $class: 'GitSCM', 
        		    branches: [[name: '*/master']], 
        		    doGenerateSubmoduleConfigurations: false, 
        		    extensions: [[$class: 'CleanCheckout']], 
        		    submoduleCfg: [], 
        	            userRemoteConfigs: [[credentialsId: 'RajaTest', url: 'https://github.com/kraja2002/helloworld.git']]
    		])
			}
		}
	}
    }
}
