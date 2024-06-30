pipeline{
    tools{
        jdk 'myjava'
        maven 'mymaven'
    }
	agent any
      stages{
           stage('Checkout with git'){
              steps{
		 echo 'cloning..'
                 git 'https://github.com/LindaMADU/JUNEDEVOPS1CLASS.git'
              }
          }
          stage('Compile with mvn1'){
              steps{
                  echo 'compiling..'
                  sh 'mvn compile'
	      }
          }
          stage('CodeReview with mvn'){
              steps{
		    
		  echo 'codeReview'
                  sh 'mvn pmd:pmd'
              }
          }
          
          stage('Package with mvn'){
              steps{
                  sh 'mvn package'
              }
          }
      }
}
