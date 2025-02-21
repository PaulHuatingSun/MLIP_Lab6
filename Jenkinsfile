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

                # TODO fill out the path to conda here
                # Initializing Conda environment
                
                sudo /home/team19/miniconda3/bin/conda init

                # TODO Complete the command to run pytest
                # Running pytest inside the Conda environment
                sudo /home/team19/miniconda3/bin/conda run -n my_env pytest --maxfail=1 --disable-warnings

                echo 'pytest executed successfully'
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
