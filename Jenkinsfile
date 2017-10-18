pipeline {
    agent any
    	 environment {
        	VERSION = VersionNumber([projectStartDate: '2017-08-01',versionNumberString: '${BUILDS_ALL_TIME}', versionPrefix: '']);	
				}
	/*parameters
	  {	
	    string(name: 'VERSION', defaultValue: 'VERSION', description: 'pass version value')

	  } */
    stages {
      
    stage('version')
 	 {
	    steps
	    {
	    build job: 'test\branch1' , wait: false, parameters: [string(name: 'VERSION', value: params.VERSION), string(name: 'PASS_VERSION', value: env.VERSION)]
	    sh "echo '$VERSION'"
	        
	    }
 	 }
  }
}
