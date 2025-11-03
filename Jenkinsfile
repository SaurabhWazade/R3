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
  sudo git clone https://github.com/SaurabhWazade/R3.git
  sudo rm -rf /var/www/html/*
  sudo /mnt/jenkins-slave/workspace/slave/R3/index.html /var/www/html/
  cd
  sudo chmod -R 777 /var/www/html/
  sudo systemctl restart httpd"""
}
      
    }
  }
}
