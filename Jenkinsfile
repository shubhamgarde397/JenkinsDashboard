def workspace;

pipeline
{
	agent any

	stages{

		stage('Preparation'){

			steps{
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
		stage('Uploading to Nexus Repo')
		{
			steps{
			echo 'Copying to nexas repo'
			}
		}
		stage('Deployment')
		{
			steps{
			bat 'xcopy C:\\ISA\\isa\\nextGen\\dist C:\\Deployment /O /X /E /H /K'
			dir('C:\\Deployment') 
				{
					bat 'rmdir /q /s dist-nextGen-old'
					bat 'ren dist-nextGen dist-nextGen-old'
					bat 'ren nextGen dist-nextGen'
				}
			
			}
		}
	}
}


    
       
