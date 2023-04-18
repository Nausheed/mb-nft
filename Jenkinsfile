#!/usr/bin/env groovy

properties([
  parameters([
    choice(
      name: 'SNode',
      choices: "100.108.42.104\n100.108.42.236",
      description: 'Select a Stage Node to Deploy'
    ),
    choice(
      name: 'Action',
      choices: "Deploy\nRollback",
      description: 'Deploy or Rollback'
    )
  ])
])

pipeline {
    agent any

    stages {
        stage('Stop Httpd') {
             when {
                expression {
                    return params.action == 'Deploy' 
                }
            }

            steps {
                script {            
                    echo "stop httpd"
                }                
            }
        }
        stage('Copy to Stage') {
            when {
                expression {
                    return params.action == 'Deploy' 
                }
            }
            steps {
                script {            
                   echo "copy to stage"
                }                
            }
        }
        stage('BackUp') {
            when {
                expression {
                    return params.action == 'Deploy' 
                }
            }
            steps {
                script {
                   echo "backup"
                }   
            }
        }
        stage('Composer') {
            when {
                expression {
                    return params.action == 'Deploy' 
                }
            }
            steps {
                script {
                    echo "composer"
                }   
            }
        }
        stage ('npm') {    
            when {
                expression {
                    return params.action == 'Deploy' 
                }
            }        
            steps {
                script {
                    echo "npm"
                }
            }
        }
        stage ('Artifacts') {
            when {
                expression {
                    return params.action == 'Deploy' 
                }
            }
            steps {
                script {
                    echo "artifacts"
                }
            }
        }
        stage ('Drush') {
            when {
                expression {
                    return params.action == 'Deploy' 
                }
            }
            steps {
                script {
                    echo "drush"                  
                }
            }
        }
        stage('Start Httpd') {
            when {
                expression {
                    return params.action == 'Deploy' 
                }
            }
            steps {
                script {            
                    echo "start httpd"
                }                
            }
        }
    }
}
