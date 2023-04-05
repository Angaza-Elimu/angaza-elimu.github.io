---
title: "Installation & Running Guide" 
weight: 7
draft: false
pre : "<b>4. </b>"
---

The main option to install the library is downloading it from github from the following [link](https://github.com/Angaza-Elimu/learning_recommendation).

Or simply running the following command.

        git clone https://github.com/Angaza-Elimu/learning_recommendation

from there change directory to the repository's folder.

        cd learning_recommendation

and install the application dependencies from the requirements file.

        pip install -r requirements.txt

afterwards you may run the database migrations.

        python3 manage.py migrate

then run the server with the following command.

        python3 manage.py runserver
