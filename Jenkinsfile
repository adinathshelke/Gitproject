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
				 sh " docker stop container11"
				  sh "docker rm container11"      
		  sh "docker run --name container11 -itdp 100:80 httpd"
				  }
		            }
					stage ('deploy index') {
				steps {
					sh "chmod -R 777 index.html"
					sh "docker cp index.html container11:/usr/local/apache2/htdocs"
					
				}	
			    }
				
			   
			   }
			   
		
		}
