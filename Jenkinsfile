pipeline
{
	agent any
	environment 
  	{
      		ANDROID_HOME = "/Users/1024257/Library/Android/sdk"
    	}
	stages
	{
		stage('build android')
		{
			steps
			{
				script
				{
					nodejs = tool name 'node11'
					sh label: '', script: "${nodejs}/npm install"
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
