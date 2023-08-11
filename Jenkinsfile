pipeline {
		 agent {
           label{
		      label "master"
			  customWorkspace "/mnt/adinath/23Q3"
		       }
		 }
		 stages{
		 stage ("create container "){
		          steps {
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
