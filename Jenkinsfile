stages {
    stage('Pull from GitHub') {
        steps {
            git branch: 'main', url: 'https://github.com/student-Alizaa/apache-site.git'
        }
    }

    stage('Deploy to Apache') {
        steps {
            sh 'sudo mkdir -p /var/www/myapp'
            sh 'sudo cp -r * /var/www/myapp/'
            sh 'sudo chown -R www-data:www-data /var/www/myapp'
            sh 'sudo systemctl reload apache2'
        }
    }
}


