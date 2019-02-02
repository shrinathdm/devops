node{
   stage('SCM Checkout'){
     git 'https://github.com/shrinathdm/devops.git'
   }
   stage('Compile-Package'){
      // Get maven home path
      def mvnHome =  tool name: 'maven-3.3', type: 'maven'   
      sh "${mvnHome}/bin/mvn package"
   }
   
    stage('Email Notification'){
    emailext attachLog: true, body: '''Hi,

     Welcome to jenkins email alerts

     Thanks,
     Shrinath''', subject: 'jenkins alert', to: 'shrinathdm@gmail.com'
   }
}


