pipeline {
		 agent {
           label{
		      label "master"
			  customWorkspace "/mnt/keshav"
		       }
		 }
	
		 stages{
		 stage ("create container "){
		          steps {
				 sh " docker stop container17"
				  sh "docker rm container17"
				  
			 sh "docker run --name container17 -itdp 90:80 httpd"
				  }
		            }
					stage ('deploy index') {
				steps {
					sh "chmod -R 777 index.html"
					sh "docker cp index.html container17:/usr/local/apache2/htdocs"
					
				}	
			    }
				
			   
			   }
			   
		
		}
