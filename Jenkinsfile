        pipeline {
    agent {
        dockerfile {
            args '-v $HOME/.m2:/root/.m2'
        }
    }
    
    environment{

        CC = 'clang'

    }
    stages {
	    
        stage('build') {
            steps {
               git url: 'https://github.com/vekatkriish/javaenv.git'
                sh "mvn clean package"
                sh "cd target && ls -al"  
                sh "echo $CC"
            }
        }
    }
}