pipeline{
	agent any
	stages{
		stage("run frontend"){
			steps{
				echo 'executing yarn...'
				nodejs(NodeJS 22.6.0){
					sh 'yarn install'
				}
			}
		}
		stage("run backend"){
			steps{
				echo 'executing gradle'
				withGradle(){
					sh './gradlew -v'
				}
			}
		}
	}
}
