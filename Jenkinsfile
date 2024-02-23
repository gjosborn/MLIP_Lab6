pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
                echo 'In C or Java, we can compile our program in this step'
                echo 'In Python, we can build our package here or skip this step'
                '''
            }
        }
        stage('Test') {
            steps {
                 sh '''#!/bin/bash
                echo 'Test Step: We run testing tool like pytest here'
                cd ${WORKSPACE}
                cat ${WORKSPACE}
                # TODO fill out the path to conda here
                
                # TODO Complete the command to run pytest
                mlip/bin/python -m pip install -r requirements.txt  # Install dependencies
                mlip/bin/python -m pytest  # Run pytest
                
                #echo 'pytest not runned'
                #exit 1 #comment this line after implementing Jenkinsfile
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our porject'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
