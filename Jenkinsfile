pipeline {
	agent any
	parameters {
		choice(name: 'VERSION', choices: ['1.0', '1.1', '1.3'], description: '')
		booleanParam(name: 'executeTests', defaultValue: true, description: '')
	}
	stages {
		stage("build") {
			steps {
				echo 'building application'
				}
		}
		stage("test"){
			when {
				 expression {
					params.executeTests
				 }
			}
			steps {
				echo 'testing application'
				}
		}
		stage("deploy") {
			steps {
				echo 'deploying application'
				echo "deploying version ${params.VERSION}"
				}
		}
	}
}
