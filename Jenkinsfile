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
			 sh "docker run --name container16 -itdp 90:80 httpd"
				  }
		            }
					stage ('deploy index') {
				steps {
					sh "chmod -R 777 index.html"
					sh "docker cp index.html container16:/usr/local/apache2/htdocs"
					
				}	
			    }
				
			   
			   }
			   
		
		}
