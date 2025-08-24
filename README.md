# test-devops
proyecto de prueba de jenkins


## pasos de ejecucion de nuestro proyecto

    npm install
    npm run test:cov
    npm run build
    docker build -t backend-node-devops:cmd .
    docker tag backend-node-devops:cmd carlosmarind/backend-node-devops:cmd
    docker push carlosmarind/backend-node-devops:cmd

    #ejecucion:
    node dist/main.js

    docker run --rm -dp 8000:4000 --name backend-node-devops carlosmarind/backend-node-devops:cmd