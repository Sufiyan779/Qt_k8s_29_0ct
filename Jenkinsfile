pipeline{
    agent { label "eksctl"}

  stages{
    stage("git checkout"){
        steps{
             git url:"https://github.com/Sufiyan779/Qt_k8s_29_0ct.git", branch:"main"
        }
    }
    stage("creating cluster"){
        steps{
             sh 'eksctl create cluster -f cluster.yaml'
        }
    }
  }  
}