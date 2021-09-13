node{
  stage('Select Server') {
    echo "Please select the server you want to Migrate: ${params.Servers}" // interperlation
    properties([[$class: 'DatadogJobProperty', emitSCMEvents: false], parameters([choice(choices: 'soafrdp13.verizon.com\nsoafrdp14.verizon.com\nsoafrdp15.verizon.com', description: 'Servers for release', name: 'Servers')])])
  }
  stage('SCM Checkout'){
    
    git 'https://github.com/prion4362/Jenkins'
  }
  stage('Compile Package'){
    sh 'mvn package'
    // echo 'test'
  }
  // Still need to update SMPT server for google mail
  stage('Email Notification') {
    mail bcc: '', body: 'This is a test email from Jenkins.', cc: 'prion4362@hotmail.com', from: '', replyTo: '', subject: 'Jenkins Test Email', to: 'prion4362@gmail.com'
  }
  
}
