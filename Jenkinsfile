pipeline {
  agent any
  tools {nodejs "node"}
  stages {
    stage('Build') {
      steps {
        git 'https://github.com/guiRodrigues/todo-tdd'
        sh 'npm install'
        sh 'npm run test'
      }}}}
