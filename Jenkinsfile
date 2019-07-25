pipeline
{
	agent any

	stages
	{
		stage('Build')
		{
				steps
				{
					"cd..".execute();
					"cd..".execute();
					"cd ISA/isa/DevUI".execute();
					"npm run ng build --prod --aot".execute();
				}
		}

	}
}