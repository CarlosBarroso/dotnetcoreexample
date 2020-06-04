pipeline{
	node('DOTNETCORE'){
		stages {
			stage('SCM'){
				steps {
					checout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations:false, extension: [], submodueCfg: [], userRemoteConfigs: [[url: 'https://github.com/CarlosBarroso/dotnetcoreexample']]])
				}
			}
			stage('build'){
				steps {
					sh 'dotnet build ConsoleApp1'
				}
			}
			stage('test'){
				steps {
					echo 'execute tests'
				}
			}
			stage('package'){
				steps {
					echo 'package'
				}
			}
			stage('deploy'){
				steps {
					echo 'deploy'
				}
			}
		}
	}
}