pipeline {
		 agent {
			 label {
		      label "master"
			  customWorkspace "/mnt/Multibranch/23Q1"
		       }
		 }
		 stages{
		 stage ("create container ") {
		          steps {
				  sh "docker run --name container1 -itdp 60:80 httpd"
				  }
		            }
					stage ('deploy index') {
				steps {
					sh "chmod -R 777 index.html"
					sh "docker cp index.html container1:/usr/local/apache2/htdocs"
					
				}	
			    }
				
			   
			   }
			   
		
		}
