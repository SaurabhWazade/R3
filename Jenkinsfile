pipeline {
  agent {
    label {
      label "QA"
    }
  }
  stages {
    stage ('one') {
steps {
  sh """sudo yum install httpd -y
  sudo systemctl start httpd
  sudo rm -rf /var/www/html/*
  sudo cp /mnt/jenkins-slave/workspace/slave/R3/index.html /var/www/html/
  cd
  sudo chmod -R 777 /var/www/html/
  sudo systemctl restart httpd"""
}
      
    }
  }
}
