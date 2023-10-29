pipeline{
    agent { label "eksctl"}

  stages{
    stage("git checkout"){
        step{
             git url:"https://github.com/Sufiyan779/Qt_k8s_29_0ct.git", branch:"master"
        }
    }
    stage("creating cluster"){
        step{
             sh 'eksctl create cluster -f cluster.yaml'
        }
    }
  }  
}