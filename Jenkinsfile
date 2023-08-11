pipeline {
		 agent {
       label{
		      label "master"
			  customWorkspace "/mnt/adinath/23Q2"
		       }
		 }
		 stages{
		 stage ("create container "){
		          steps {
				   sh  "docker kill container2"
					sh "docker rm container2"
				  sh "docker run --name container2 -itdp 70:80 httpd"
				  }
		            }
					stage ('deploy index') {
				steps {
					sh "chmod -R 777 index.html"
					sh "docker cp index.html container2:/usr/local/apache2/htdocs"
					
				}	
			    }
				
			   
			   }
			   
		
		}
