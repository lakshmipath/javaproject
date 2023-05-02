pipeline{
    
    
    
    
    agent any
    
    stages{
        
        stage('stage-1'){
            
            steps{
                
                git 'https://github.com/lakshmipath/javaproject.git'
            }
        }
        stage('stage-2'){
            steps{
                sh 'mvn package'
                
            }
            
        }
        stage('stage-3'){
            steps{
                sshagent(['jenkinspipelinefordeclarative']) {
             sh 'scp -o StrictHostKeyChecking=false target/javaproject.war ec2-user@44.201.130.17:/opt/apache-tomcat-9.0.74/webapps/'
}
                
            }
            
        }
        
    }
    
    
}
