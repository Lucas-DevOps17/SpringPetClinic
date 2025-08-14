pipeline {
    agent any
    tools { maven "M3" }

    stages {
        stage("checkout") {
            steps {
                git branch: "main", url: "https://github.com/Lucas-DevOps17/SpringPetClinic.git"
            }
        }

        stage("build") {
            steps {
                bat "mvn compile"
            }
        }

        stage("test") {
            steps {
                bat "mvn test"
            }
        }

        stage("package") {
            steps {
                bat "mvn package -DskipTests"
                bat "dir target"
            }
        }

        stage("deploy") {
            steps {
                bat "java -jar target/spring-petclinic-2.1.0.BUILD-SNAPSHOT.jar"
            }
        }
    }
}
