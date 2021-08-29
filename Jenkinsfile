pipeline{
agent any
stages{
    stage("code checkout"){
        steps{
            script{
               git credentialsId: '7a815742-dc36-41fc-ba7f-eae204ecec91', url: 'https://github.com/saikiran1095/sparkjava-war-example.git' 
            }
        }
    }
    stage("build & compile"){
        steps{
            script{
               withMaven(jdk: 'java', maven: 'maven') {
    sh 'mvn clean install -DskipTests'
} 
            }
        }
    }
}
}
