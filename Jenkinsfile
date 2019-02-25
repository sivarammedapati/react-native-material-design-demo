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
					tools 
					{
   			 			nodejs 'node11'
  					}
					sh label: '', script: 'npm install react-native-android-statusbar'
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
