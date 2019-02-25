pipeline
{
	agent any
	environment 
  	{
      		ANDROID_HOME = "/Users/1024257/Library/Android/sdk"
		PATH = "$PATH:/usr/local/lib/node_modules/npm/bin/npm-cli.js"
    	}
	stages
	{
		stage('build android')
		{
			steps
			{
				script
				{
					sh label: '', script: '/usr/local/lib/node_modules/npm/bin/npm-cli.js install — production'
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
