    // stage("git checkout"){
    //     steps{
    //          git url:"https://github.com/Sufiyan779/Qt_k8s_29_0ct.git", branch:"main"
    //     }
    // }
    // stage("creating cluster"){
    //     steps{
    //          sh 'eksctl create cluster -f cluster.yaml'
    //     }
    // }
   
pipeline {
    agent any

    triggers {
        pollSCM('* * * * *') // Poll the SCM every minute
    }

    stages {
        stage('Check and Create Folder') {
            steps {
                script {
                    def folderName = 'abc'
                    def folderExists = fileExists(folderName)

                    if (folderExists) {
                        echo "Folder $folderName already exists"
                    } else {
                        echo "Folder $folderName does not exist. Creating..."
                        sh "mkdir $folderName"
                    }
                }
            }
        }
    }
 