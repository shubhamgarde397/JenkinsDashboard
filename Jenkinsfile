def workspace;

pipeline
{
	agent any

	stages{

		stage('Preparation'){

			steps{
				echo 'Files e in preparation State'
			}
		}

		stage('build') 
		 {
            steps 
			{
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
			steps
			{
				bat 'xcopy C:\\ISA\\isa\\nextGen\\dist C:\\Deployment /O /X /E /H /K'
				dir('C:\\Deployment') 
					{
						bat 'rmdir /q /s dist-nextGen-old'
						bat 'ren dist-nextGen dist-nextGen-old'
						bat 'ren nextGen dist-nextGen'
					}
				dir('C:\\Deployment\\dist-nextGen')
				{
					bat 'xcopy C:\\Deployment\\dist-nextGen\\index.html C:\\Deployment /s /h /e /k /f /c'
				}
				dir('C:\\Deployment')
				{
					bat 'del index-nextGen-old.html'
					bat 'ren index-nextGen.html index-nextGen-old.html'
					
				}
				dir('C:\\Deployment')
				{
					bat 'ren index.html index-nextGen.html'
					bat 'C:\\Users\\shubham.nitin.garde\\AppData\\Local\\Programs\\Python\\Python37-32\\python.exe C:\\Deployment\\file.py nextGen'
					bat 'del index-nextGen.html'
					bat 'ren index-2-nextGen.html index-nextGen.html'
				}
				dir('C:\\ISA\\isa\\nextGen')
				{
					bat 'rmdir /q /s dist'
				}
			}
		}
	}
}


    
       
