node{
   stage('SCM Checkout'){
     git 'https://github.com/shrinathmangalore/devops.git'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'maven-3.3', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
}


