pipeline {
  agent any
  
  environment {
        NAME='Pepe'
        VERSION = '1'
  }
  
  stages {
    stage('stage1') {
      steps {
        
        // Variables inside a single quoted string don't get expanded eg
        echo 'This is the $BUILD_NUMBER of version $VERSION'
        // In BlueOcean, insert the echo command through a Shell Script step
        echo "This is the $BUILD_NUMBER of version $VERSION"
        
        sh '''
          echo "Using a multi-line shell step"
          chmod +x test.sh
          ./test.sh
        '''
        
      }
    }

  }

}
