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
    stage("clone"){
      steps{
      echo "cloning"
      }
    }
  }
}
