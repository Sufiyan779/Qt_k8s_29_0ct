pipeline{
    agent { label "eksctl"}
      triggers {
        pollSCM('* * * * *') // Poll SCM every minute (use your desired cron schedule)
    }
  stages{
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
     stage('Check and Create Folder') {
            steps {
                script {
                    def folderName = 'abc'
                    def folderExists = fileExists(folderName)

                    if (folderExists) {
                        echo "Folder $folderName already exists"
                    }
                    else {
                        echo "Folder $folderName does not exist. Creating..."
                        sh "mkdir $folderName"
                    }
                }
            }

    }
  }
   
   }