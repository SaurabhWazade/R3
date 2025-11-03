pipeline {
  agent {
    label {
      label "QA"
    }
  }
  stages {
    stage ('one') {
steps {
  sh """yum install httpd -y
  systemctl start httpd
  git clone https://github.com/SaurabhWazade/R3.git
  rm -rf /var/www/html/*
  cp /root/.jenkins/workspace/'test 2'/R3/index.html /var/www/html/
  cd
  chmod -R 777 /var/www/html/
  systemctl restart httpd"""
}
      
    }
  }
}
