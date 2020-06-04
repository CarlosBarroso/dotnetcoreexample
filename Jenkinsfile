node('dotnetcore'){
	stage('SCM'){
		checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations:false, extension: [], submodueCfg: [], userRemoteConfigs: [[url: 'https://github.com/CarlosBarroso/dotnetcoreexample']]])
	}
	stage('pre-build'){
		sh 'dotnet --info'
	}
	stage('build'){
		sh 'dotnet build ConsoleApp1'
	}
	stage('test'){
		echo 'execute tests'
	}
	stage('package'){
		echo 'package'
	}
	stage('deploy'){
		echo 'deploy'
	}
	stage('Archive'){
		archiveArtifacts artifacts: 'ConsoleApp1/*.*'
	}
}