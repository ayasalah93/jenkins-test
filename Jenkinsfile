pipeline {
    agent any
	parameters
	  {	VERSION = VersionNumber projectStartDate: '2017-09-13', versionNumberString: '${BUILDS_ALL_TIME}', versionPrefix: '0.0.'
	    string(name: 'VERSION', defaultValue: '${env.VERSION}', versionPrefix: '0.0.'', description: 'pass version value')

	  }
    stages {
    stage('version')
 	 {
	    steps
	    {
	    build job: 'test\branch1' , wait: false, parameters: [string(name: 'VERSION', value: params.VERSION), string(name: 'PASS_VERSION', value: env.VERSION)]
	    }
 	 }
  }
}
