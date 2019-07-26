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
				sh label: '', script: 'cd\\'
				sh label: '', script: 'cd Projects\\NRCM'
				dir('C:\\Projects\\NRCM\\') 
				{
					echo 'hi'
                	sh 'npm run ng build --prod --aot'
            	}
        	}
		}
	}
}


    
       
