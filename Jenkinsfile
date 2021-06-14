pipeline { //indicate the job is written in Declarative Pipeline
agent any //agent specifies where the pipeline will execute. 
   stages {
stage ("Execute the test suite"){
steps {
sh '''
				cd /opt/jenkins/Katalon_Studio_Engine_Linux_64-7.9.1
                 ./katalonc -noSplash -runMode=console -projectPath="$WORKSPACE/FlipkartApp.prj" -retry=0 -testSuitePath="Test Suites/TestSuite1" -executionProfile="default" -browserType="Chrome" -apiKey="6e2b1a4d-750f-419c-b58e-960d52d7877c" --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true
 	'''
		
		}
		}
		}
		
	       post {
	always {
		cleanWs()
		   }
	     }
}
