pipeline {
    agent any

    stages {
        stage('Сборка') {
            steps {
                echo 'Выполняем команды для сборки'
		echo "Текущий агент: ${env.NODE_NAME}"
    		echo "Рабочая директория: ${env.WORKSPACE}"
    		sh 'uname -a'  // Информация о системе
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
    }
