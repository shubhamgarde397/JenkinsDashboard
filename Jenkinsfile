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
				//  sh 'npm --version'
			bat 'xcopy C:\\PYTHON C:\\Projects /O /X /E /H /K'
			bat 'cd\\'
			bat 'cd C:\\ISA\\isa\\nextGen'
			bat 'npm run ng build --prod --aot'
        	}
		}
	}
}


    
       
