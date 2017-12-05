        pipeline {
    agent {
        dockerfile {
            args '-v $HOME/.m2:/root/.m2'
        }
    }
    
    environment{

        CC = 'clang'
        id=BUILD_ID

    }
    stages {
	    
        stage('build') {
            steps {
               git url: 'https://github.com/vekatkriish/javaenv.git'
                sh "mvn clean package"
                sh "cd target && ls -al"  
                sh "echo $CC"
                sh "echo id"
            }
        }
    }
}
