pipeline {

  agent any
  
  tools {
    maven 'Maven3'
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
