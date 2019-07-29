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
			// bat 'xcopy C:\\PYTHON C:\\Projects /O /X /E /H /K'
			dir('C:\\ISA\\isa\\nextGen') {
				bat label: '', script: 'npm run ng build --prod --aot'
			}
			// bat label: '', script: 'cd\\'
			// bat label: '', script: 'cd C:\\ISA\\isa\\nextGen'
			// bat label: '', script: 'cd'
			// bat label: '', script: 'npm run ng build --prod --aot'
        	}
		}
	}
}


    
       
