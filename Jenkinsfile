pipeline {

  agent any
  environment {
    NEW_VERSION = '2.0.0'
  }
  parameters {
    choice(name: 'VERSION', choices: ['1.0.0', '1.1.0'], description: '')
  }
  
  tools {
    maven 'Maven3'
  }
  
  stages { 
    stage("build") { 
      steps {
        echo "In Build section"
        echo "Building version: ${NEW_VERSION}"
      }
    }
    
    
    stage("test") { 
      when {
        expression {
          BRANCH_NAME == 'dev'
        }
      }
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
  
  post {
    always {
      echo "Always Showing this"
    }
    success {
      echo "Showing this only because I'm success"
      echo "Version selected: ${param.VERSION}"
    }
  }
}
