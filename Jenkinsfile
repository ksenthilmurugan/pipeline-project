pipeline {

  agent any

  parameters {
    choice(name: 'VERSION', choices: ['1.0.0', '1.1.0'], description: '')
  }

  
  stages { 
    stage("build") { 
      steps {
        echo "In Build section"
        
      }
    }
    
    
    stage("test") { 
      when {
        expression {
          BRANCH_NAME == 'master'
        }
      }
      steps {
        echo "In test section"
        echo "Version selected: ${params.VERSION}"
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
      echo "Version selected: ${params.VERSION}"
    }
  }
}
