pipeline { //indicate the job is written in Declarative Pipeline
agent any //agent specifies where the pipeline will execute. 
   stages {
stage ("Execute the test suite"){
steps {
sh '''
				cd /opt/Katalon_Studio_Engine_Linux_64-8.0.5
                 ./katalonc -noSplash -runMode=console -projectPath="$WORKSPACE/FlipkartApp.prj" -retry=0 -testSuitePath="Test Suites/TestSuite1" -executionProfile="default" -browserType="Chrome" -apiKey="497b0e47-1311-484b-910f-aa4a9dde66e1" --config -proxy.auth.option=NO_PROXY -proxy.system.option=NO_PROXY -proxy.system.applyToDesiredCapabilities=true
		
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
