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
                script {
                    def disk_size = sh(script: "df / --output=avail | tail -1", returnStdout: true).trim() as Integer
                    println("disk_size = ${disk_size}")
                }
			}
		}
	}
}
