pipeline {
		 agent {
           label{
		      label "master"
			  customWorkspace "/mnt/keshav"
		       }
		 }
	tools {
           git "2.40.1"
		
	}
		 stages{
		 stage ("create container "){
		          steps {
				 /*  sh  "docker kill container3"
					sh "docker rm container3" */
				  sh "docker run --name container3 -itdp 90:80 httpd"
				  }
		            }
					stage ('deploy index') {
				steps {
					sh "chmod -R 777 index.html"
					sh "docker cp index.html container3:/usr/local/apache2/htdocs"
					
				}	
			    }
				
			   
			   }
			   
		
		}
