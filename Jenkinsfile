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
				   sh " docker stop container13"
				  sh "docker rm container13"
				 sh "docker run --name container13 -itdp 70:80 httpd"
				  }
		            }
					stage ('deploy index') {
				steps {
					sh "chmod -R 777 index.html"
					sh "docker cp index.html container13:/usr/local/apache2/htdocs"
					
				}	
			    }
				
			   
			   }
			   
		
		}
