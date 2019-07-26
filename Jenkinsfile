def workspace;

pipeline
{
	agent any

	stages
	{
		 stage('build') 
		 {
            steps 
			{
				dir('C:\\Projects\\NRCM\\') 
				{
					echo 'hi'
                	sh 'npm run ng build --prod --aot'
            	}
        	}
		}
	}
}


    
       
