# Model used gpt-4o/claude-3.5-sonnet

En este ejercicio vamos a trabajar en la creación de un pipeline en GitHub Actions que nos permitirá pasar unos tests de backend, generar un build y desplegar el backend en un EC2. El pipeline se disparará con un push a una rama con un Pull Request abierto.

Pre-requisitos:

    🔗 Añadir keys a github actions para desplegar automáticamente en AWS -> https://lightrains.com/blogs/deploy-aws-ec2-using-github-actions/ 

Tu misión en este ejercicio es crear un pipeline en GitHub Actions que, tras el trigger "push a una rama con un Pull Request abierto", siga los siguientes pasos:

    Pase unos tests de backend.
    Genere un build del backend.
    Despliegue el backend en un EC2. 

Para ello, debes seguir estos pasos:

    Configurar el workflow de GitHub Actions en un archivo .github/workflows/pipeline.yml.
    Documentar los prompts utilizados para generar cada paso del pipeline:
        Tests de backend.
        Generación del build del backend.
        Despliegue del backend en EC2.
    Asegúrate de que el pipeline se dispare con un push a una rama con un Pull Request abierto.