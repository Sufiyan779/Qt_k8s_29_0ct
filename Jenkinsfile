pipeline{
    agent { label "eksctl"}
    triggers{
        pollSCM("* * * * *")
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
        stage("when condition"){
            steps{
                script{
                def folder="abc"
                def folderstatus= fileExists(folder)

                if (folderstatus){
                    echo "${folder}: already folder exist"
                }
                else{
                    echo "${folder}: Does not exist"
                    sh "mkdir /home/ubuntu/${folder}"
                }
                }
            }

    }
  }  
}