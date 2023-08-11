pipeline {
		 agent {
			 label {
		      label "master"
			  customWorkspace "/mnt/keshav"
		       }
		 }
		 stages{
		 stage ("create container ") {
		          steps {
				 sh " docker stop container12"
				  sh "docker rm container12" 
				sh "docker run --name container12 -itdp 60:80 httpd"
				  }
		            }
					stage ('deploy index') {
				steps {
					sh "chmod -R 777 index.html"
					sh "docker cp index.html container12:/usr/local/apache2/htdocs"
					
				}	
			    }
				
			   
			   }
			   
		
		}
