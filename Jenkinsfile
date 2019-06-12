node('maven-label'){
    def mvnHome
    stage("preparation"){
        //test
        git 'https://github.com/Raghu0007/abc.git'
        mvnHome = tool 'maven'
    }
        stage("build"){
            if (isUnix()){
                sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
            }else {
                bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
            }
              
    }
        stage("Results"){
            junit '**/target/surefire-reports/TEST-*.xml'
            archive 'target/*.jar'
    }
        stage("3"){
        
    }
        stage("5"){
        
    }
}
