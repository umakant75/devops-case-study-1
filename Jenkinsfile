pipeline {
 agent any
 stages{
      stage('checkout')
      {
          steps{
                 git 'https://github.com/umakant75/devops-case-study-1.git'
               }
      }
  
   stage('Build & Run Junit'){
         steps{
        withMaven(maven:'MyMaven'){
          dir('DevOpsCaseStudy'){
            sh 'chmod +x src/main/resources/chromedriver'
            sh '''
            mvn clean install -B -U -q -Dmaven.test.failure.ignore=true -DskipTests
            '''
           
          }
         }
        }
      }
  
  
  /*****/
 
     } 
}
