pipeline
{
	ageny any
	stages
	{
		stage('build android')
		{
			steps
			{
				dir("android") 
				{
    					sh label: '', script: './gradlew assembleRelease'
				}	
			}
		}
	}
}
