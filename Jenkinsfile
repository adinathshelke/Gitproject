pipeline {
		 agent {
           label{
		      label "master"
			  customWorkspace "/mnt/adinath/master"
		       }
		 }
		 stages{
		 stage ("create container "){
		          steps {
				       sh  "docker kill container0"
					sh "docker rm container0"

				  sh "docker run --name container0 -itdp 100:80 httpd"
				  }
		            }
					stage ('deploy index') {
				steps {
					sh "chmod -R 777 index.html"
					sh "docker cp index.html container0:/usr/local/apache2/htdocs"
					
				}	
			    }
				
			   
			   }
			   
		
		}
