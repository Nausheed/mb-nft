properties([
  parameters([
    choice(
      name: 'SNode',
      choices: "100.108.42.104\n100.108.42.236",
      description: 'Select a Stage Node to Deploy'
    ),
    choice(
      name: 'action',
      choices: "Deploy\nRollback",
      description: 'Select deployment action'
    )
  ])
])



pipeline{
  agent any
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
