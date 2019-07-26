def workspace;

pipeline
{
	agent any

	stages
	{
		 stage('build') {
            steps {
				dir('C:\\ISA\\isa\\DevUI') {
                sh 'npm run ng build --prod --aot'
            }
        }
	}
}


    
       
