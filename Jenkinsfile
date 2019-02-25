pipeline
{
	agent any
	tools 
	{
    		nodejs 'node11'
  	}
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
					sh label: '', script: 'npm install'
					sh label: '', script: 'npm install react-native'
					sh label: '', script: 'npm install react-native-cli'
					
					jdk = tool name: 'java8'
  					env.JAVA_HOME = "${jdk}"
					dir("android") 
					{
    						sh label: '', script: './gradlew assembleRelease --stacktrace'
					}
				}
			}
		}
	}
}
