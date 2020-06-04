pipeline {

  agent any

  parameters {
    choice(name: 'VERSION', choices: ['1.0.0', '1.1.0'], description: '')
  }

  
  stages { 
    stage("init") { 
      steps {
        echo "In Init section"
        script {
          gv = load "script.groovy"
        }
        
      }
    }
    
    stage("build") { 
      steps {
        script { 
          gv.buildStep()
        }
        
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
        script { 
          gv.testStep()
        }
      }
    }
    
    
    stage("deploy") { 
      steps {
        echo "In deploy section"
        script { 
          gv.deployStep()
        }
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
