pipeline {
    agent any
    environment {
        //be sure to replace "bhavukm" with your own Docker Hub username
        DOCKER_IMAGE_NAME = "aphashimsalim/train-schedule"
    }
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh 'sleep 150'
                //sh './gradlew build --no-daemon ; gradle --stop'
                //archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }}
        stage('Build - artifact') {
            steps {
                echo 'Running build automation -artifact'
                
                //archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
        stage('Build Docker Image') {
            //when {
            //    branch 'master'
           // }
            steps {echo 'Running build automation -artifact'
             //   script {
               //     app = docker.build(DOCKER_IMAGE_NAME)
                 //   app.inside {
                   //     sh 'echo Hello, World!'
                    //}
                //}
            }
        }
        stage('Push Docker Image') {
            //when {
              //  branch 'master'
            //}
            steps {echo 'Running build automation -artifact'
              //  script {
                //    docker.withRegistry('https://registry.hub.docker.com', 'docker_hub_login') {
                  //      app.push("${env.BUILD_NUMBER}")
                    //    app.push("latest")
                    //}
                //}
            }
        }
        stage('CanaryDeploy') {
            //when {
              //  branch 'master'
            //}
            //environment { 
              //  CANARY_REPLICAS = 1
            //}
            steps {echo 'Running build automation -artifact'
              //  kubernetesDeploy(
                //    kubeconfigId: 'kubeconfig',
                  //  configs: 'train-schedule-kube-canary.yml',
                    //enableConfigSubstitution: true
                //)
            }
        }
        stage('DeployToProduction') {
            //when {
              //  branch 'master'
            //}
            //environment { 
              //  CANARY_REPLICAS = 0
            //}
            steps {echo 'Running build automation -artifact'
              //  input 'Deploy to Production?'
               // milestone(1)
                //kubernetesDeploy(
                  //  kubeconfigId: 'kubeconfig',
                   // configs: 'train-schedule-kube-canary.yml',
                    ///enableConfigSubstitution: true
                //)
                //kubernetesDeploy(
                 //   kubeconfigId: 'kubeconfig',
                  //  configs: 'train-schedule-kube.yml',
                    //enableConfigSubstitution: true
                //)
            }
        }
    }
}
