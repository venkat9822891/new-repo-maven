node('slvnew') {
    stage('Cont.Download') {
    git 'https://github.com/venkat9822891/maven-project1.git'
      }
	stage('Cont.Build') {
    sh 'mvn package'
      }
	stage('Cont.Deploy') {
	deploy adapters: [tomcat9(credentialsId: 'dded43c3-e568-4414-a254-d2060b25fbed', path: '', url: 'http://172.31.38.129:8080')], contextPath: '/realtimeapp-test', war: '**/*.war'
	      }
}

