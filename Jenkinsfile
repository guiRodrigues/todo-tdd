pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage('Cloning Git') {
      steps {
        git 'https://github.com/guiRodrigues/todo-tdd'
      }
    }
        
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
     
    stage('Test') {
      steps {
         sh 'npm test'
      }
    }   
    
    stage('Print Message') {
      steps {
         sh 'echo "hello world"'
      }
    }  
    
    stage('Notify Discord') {
      steps {
         discordSend description: "Funcionou?", footer: "Footer Text", link: env.BUILD_URL, result: currentBuild.currentResult, title: JOB_NAME, webhookURL: "https://discord.com/api/webhooks/938499035260649563/-rl0Xds2O9f_k-rCrsIYWFCPaCbzwmGaWMF7-usaTn89FoHwzBD9aM3dzJJd6O3T8iwq"
      }
    }   
  }
}