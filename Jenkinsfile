pipeline{
      agent any
      stages{
            stage('clean'){
                  steps{
                        sh "rm -r *"
                        sh "rm -r /var/www/html/*"
                  }
            }
            stage('clone'){
                  steps{
                        sh "git clone https://gitlab.com/sanghavij243/netflix.git -b master"
                  }
            }
            stage('deploy'){
                  steps{
                        sh "mv netflix/* /var/www/html"
                  }
            }
      }
}
