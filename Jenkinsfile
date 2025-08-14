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
                bat "mvn compile"
            }
        }
        
        stage("test"){
            
            steps{
                bat "mvn test"
            }
        }
        
        stage("deploy"){
            
            steps{
                bat "java -jar C:\ProgramData\Jenkins\.jenkins\workspace\SpringPetClinic\target\*.jar"
            }
        }
    }
}
