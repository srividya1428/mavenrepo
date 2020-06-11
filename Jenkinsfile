pipeline{
agent {label 'dev'}
stages{
		stage("checkout"){
			steps{
				checkout([$class: 'GitSCM', 
    				branches: [[name: '*/master']], 
    				userRemoteConfigs: [[credentialsId: 'bc7c2e61-dd0b-4ca6-94c6-3f0bd061b89d', url: 'https://github.com/srividya1428/mavenrepo.git']]
				    ])
			      }//close steps for stage1
		    }//close for stage1
		stage("build"){
			steps{
			      sh "mvn package"
			     }//close steps for stage2
			}//close for stage2
	   	}//close for stages
}//close for pipeline
