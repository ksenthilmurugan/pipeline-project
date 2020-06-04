pipeline {

  agent any
  
  tools {
    Maven 'Maven3'
  }
  
  stages { 
    stage("build") { 
      steps {
        echo "In Build section"
      }
    }
    
    
    stage("test") { 
      steps {
        echo "In test section"
      }
    }
    
    
    stage("deploy") { 
      steps {
        echo "In deploy section"
      }
    }
  }
}
