pipeline {
    agent any

    stages {
        stage('Сборка') {
            steps {
                echo 'Выполняем команды для сборки'
            }
        }
        stage('Тестирование') {
            steps {
                echo 'Тестируем нашу сборку'
            }
        }
        stage('Развертывание') {
            steps {
                echo 'Переносим код в рабочую среду или создаем артефакт'
            }
	}
	stage('Finish') {
	    steps {
		echo 'Finish all activities'
	    }
        }
	post {
	    failure {
		mail to: 'yurgens@gamil.com',
                subject: "Build Failed: ${currentBuild.fullDisplayName}",
                body: "Проверьте вот эту вот сборку: ${env.BUILD_URL}"
	    }
	
}
    }
}
