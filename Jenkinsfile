pipeline {

  parameters {
    string(name: 'nomecartella', defaultValue: 'terraform', description: 'Nome della cartella da creare')

  }

  environment {
    AWS_ACCESS_KEY_ID = credentials('AWS_ACCESS_KEY_ID')
    AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
    TF_VAR_private_key_file = credentials('MY_KEY_PAIR_PEM')
  }

  agent any

  stages {
    stage('Creazione Cartella') {
      steps {
        sh 'pwd; cd terraform/aws-instance-first-script; mkdir ${nomecartella}'

      }
    }
  }

}
