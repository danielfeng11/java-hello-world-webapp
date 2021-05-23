// Powered by Infostretch 

timestamps {

node () {

	stage ('FirstFreestyle - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '', url: 'https://github.com/danielfeng11/java-hello-world-webapp.git']]]) 
	}
	stage ('FirstFreestyle - Build') {
 			// Maven build step
	withMaven(maven: 'mvn') { 
 			if(isUnix()) {
 				sh "mvn clean install package " 
			} else { 
 				bat "mvn clean install package " 
			} 
 		}		// Shell build step
// sh """ 
// #!/bin/bash

// echo "hello, today is $(date)" 
//  """ 
	}
}
}
