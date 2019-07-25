pipeline
{
	agent any

	stages
	{
		stage('Build')
		{
				steps
				{
					def cmd=new CommandShell()
					println cmd.execute("cd /d c:\\ISA")
					println cmd.execute("dir") // Will be the dir of c:\
				}
		}
	}
}