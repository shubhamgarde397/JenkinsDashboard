pipeline
{
	agent any

	stages
	{
		stage('Build')
		{
				steps
				{
					"cmd /c mvn".execute()
					print "cmd /c mvn".execute().text
				}
		}
	}
}