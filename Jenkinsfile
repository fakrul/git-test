pipeline {
	agent any
	stages {
		stage ('verify branch') {
			steps {
				echo "$GIT_BRANCH"
			}
		}
		stage ('hostname') {
			steps {
                script {
                    sh(script: "hostname")
                }
			}
		}
	}
		stage ('disk size - shell script') {
			steps {
                script {
                    def disk_size = sh(script: "df / --output=avail | tail -1", returnStdout: true).trim() as Integer
                    println("disk_size = ${disk_size}")
                }
			}
		}
	}
}
