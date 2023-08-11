pipeline {
		 agent {
       label{
		      label "master"
			  customWorkspace "/mnt/Multibranch/23Q2"
		       }
		 }
		 stages{
		 stage ("create container "){
		          steps {
				  sh "docker run --name container1 -itdp 70:80 httpd"
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
