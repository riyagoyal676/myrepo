pipeline {
    agent any
    
    environment {
        name = 'riya'
    }
    
    parameters {
        string(name: 'person' , defaultValue: 'riya goyal' , description: "who are you")
        choice(name: 'city' , choices: ['mumbai' ,'pune' ] , description: "good choice")
    }

    stages {
        stage('parameters') {
            steps {
                sh 'echo "${name}"'
                sh 'echo "${person}"'
            }
        }
        stage('Continue ?')  {
              input {
                  message "should we continue?"
                  ok "yes we should"
        }
        
            steps {
                echo 'testt'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying'
            }
        }
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
    }
     post{
         always{
             echo "i will always say hello again!"
         }
     }
}

