pipeline
{
	agent any

	stages
	{
		stage('Build')
		{
				steps
				{
					Console console=System.console();
					def name=console.readLine("What is your name? ")
					println "Welcome to Groovy, $name!"
				}
		}
	}
}