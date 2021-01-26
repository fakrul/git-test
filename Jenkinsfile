pipeline {
	agent any
	stages {
		stage ('Verify Branch') {
			steps {
				echo "$GIT_BRANCH"
			}
		}
		stage ('Shell Scritp') {
			steps {
				sh (script: ifconfig.sh)
			}
		}
	}
}
