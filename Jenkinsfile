node{
  stage('SCM Checkout'){ 
    git 'https://github.com/prion4362/Jenkins'
  }
  stage('Compile Package'){
    sh 'mvn package'
    // echo 'test'
  }
  
}
