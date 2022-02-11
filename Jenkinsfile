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
		  
variables:
MSBUILD_PATH: 'C:\Program Files (x86)\Microsoft Visual Studio\2019\Professional\MSBuild\Current\Bin\amd64\MSBuild.exe'
VSTEST_PATH: 'C:\Program Files (x86)\Microsoft Visual Studio\2019\Professional\Common7\IDE\Extensions\TestPlatform\vstest.console.exe'

stages:
  - build
  - test

build-job:
  only:
  - web
  stage: build
  script:
    - echo "Building..."
    - '& "$env:MSBUILD_PATH" -restore /p:Platform=x64'
  artifacts:
    paths:
      - <project1>\bin
      - <project2>\bin
  test-job1:
	}
    }
}
