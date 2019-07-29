def workspace;

pipeline
{
	agent any

	stages
	{
		stage('Preparation')
		{
			steps
			{
				echo 'Files are in preparation State'
			}
		}
		 stage('build') 
		 {
            steps 
			{
				//  sh 'npm --version'
				// bat 'xcopy C:\\PYTHON C:\\Projects /O /X /E /H /K'
				dir('C:\\ISA\\isa\\nextGen') 
				{
					bat label: '', script: 'npm run ng build --prod --aot'
					echo 'Build Successfull'
				}
        	}
		}
		stage('Copying to Nexus Repo')
		{
			echo 'Copying to nexas repo'
		}
		stage('Deployment')
		{
			echo 'Deployment in process'
		}
	}
}


    
       
