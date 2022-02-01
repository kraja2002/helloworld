pipeline {
	agent any 
	stage('checkout'){
    steps{
        script{
	    checkout([
        $class: 'GitSCM', 
        branches: [[name: '*/master']], 
        doGenerateSubmoduleConfigurations: false, 
        extensions: [[$class: 'CleanCheckout']], 
        submoduleCfg: [], 
        userRemoteConfigs: [[credentialsId: '<gitCredentials>', url: '<gitRepoURL>']]
    ])
			}
		}
	}
}
