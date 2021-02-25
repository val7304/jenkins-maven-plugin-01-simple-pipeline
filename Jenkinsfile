pipeline{
    agent any
    tools{
        maven 'my-maven-3'
    }
    stages{
        stage("Chekout Code from SCM"){
            steps{
                echo "========Chekout Code from SCM========"
                git url: 'https://github.com/val7304/jenkins-maven-plugin-01-simple-pipeline.git'
                    branch: 'main'
                }
        }
        stage("CleanUp"){
            steps{
                echo "======== CleanUp ========"
                sh "mvn clean"; 
            }
        }
        stage("Compile"){
            steps{
                echo "======== compile  ========"
                sh "mvn compile"; 
            }
        }        
        stage("Unit tests"){
            steps{
                echo "======== tests ========"
                sh "mvn test"; 
            }
        }

        stage("Package (i.e generale the deployable JAR))"){
            steps{
                echo "======== Package ========"
                sh "mvn package"; 
            }
        }

    }





}