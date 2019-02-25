pipeline
{
	agent any
	stages
	{
		stage('build android')
		{
			steps
			{
				script
				{
					jdk = tool name: 'java8'
  					env.JAVA_HOME = "${jdk}"
					dir("android") 
					{
    						sh label: '', script: './gradlew assembleRelease'
					}
				}
			}
		}
	}
}
