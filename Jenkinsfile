
pipeline{
  agent any
   parameters {
        choice(
            choices: 'ServerA\nServerB', 
            description: 'Select a server for deployment', 
            name: 'server'
        )
        choice(
            choices: 'Deploy\nRollback', 
            description: 'Select deployment action', 
            name: 'action'
        )
    }
  stages{
    stage("Deploy"){
      when{
        expression {
          return params.action == 'Deploy'
        }
      }
      steps{
        echo "${params.action}"
      }
    }
    
    stage("Rollback"){
      when{
        expression {
          return params.action == 'Rollback'
        }
      }
      steps{
        echo "${params.action}"
      }
    }
  }
}
