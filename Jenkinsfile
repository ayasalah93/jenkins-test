pipeline {
    agent any
    stages {
	     parameters
  {
    string(name: 'VERSION', defaultValue: '${env.VERSION}', description: 'pass version value')
   
  }
    stage('version')
  {
    steps
    {
    build job: 'BUILD/CMTest2/' + env.VERSION.replaceAll("/", "%2F"), wait: false, parameters: [string(name: 'VERSION', value: params.VERSION), string(name: 'PASS_VERSION', value: env.VERSION)]
    }
  }
  }
}

