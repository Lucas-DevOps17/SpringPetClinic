pipeline {
    
    agent any
    tools {maven "M3"}
    stages{
        
        stage("checkout"){
        
            steps{
                git branch: "main", url: "https://github.com/Lucas-DevOps17/SpringPetClinic.git"
            }
        }
 
        stage("build"){
            
            steps{
                sh "mvn compile"
            }
        }
        
        stage("test"){
            
            steps{
                sh "mvn test"
            }
        }
        
        stage("deploy"){
            
            steps{
                sh "java -jar /home/coder/,jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar"
            }
        }
    }
}
