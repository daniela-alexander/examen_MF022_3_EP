# EJERCICIO 2 
## Numeración e historial de comandos Linux utilizados en el ejercicio.

            1  apt update
            2  apt install nano tree -y
            3  mkdir dev_environment
            4  cd dev_environment
            5  mkdir -p frontend/public frontend/src/components frontend/src/pages frontend/src/styles backend/app backend/config backend/tests database/migrations docs scripts
            6  cd dev_environment
            7  ls
            8  cd frontend
            9  ls
        10  cd src
        11  ls
        12  cd .
        13  cd . .
        14  cd..
        15  cd ..
        16  touch frontend/public/index.html
        17  touch frontend/src/App.js
        18  touch frontend/src/styles/main.css
        19  touch backend/app/server.js
        20  touch backend/config/config.json
        21  touch README.md
        22  touch scripts/deploy.sh
        23  cd frontend
        24  ls
        25  cd public
        26  ls
        27  cd ..
        28  ls src
        29  cd src
        30  ls
        31  cd ..
        32  sudo apt update
        33  cd ..
        34  apt update
        35  apt install nano -y
        36  nano frontend/public/index.html
        37  ls -l frontend/public/index.html
        38  dev_environment
        39  cd dev_environment
        40  nano frontend/public/index.html
        41  nano frontend/src/App.js
        42  nano frontend/src/styles/main.css
        43  tree
        44  ls -la
        45  ls frontend/src
        46  mkdir backup
        47  cp -r frontend backup/
        48  cp backend/app/server.js backup/server_backup.js
        49  mv frontend/src/styles/main.css frontend/public/
        50  mv frontend/src/App.js frontend/src/app.js
        51  mv backend/config/config.json backend/app/
        52  chmod 700 scripts/deploy.sh 
        53  chmod 640 backend/app/server.js
        54  chmod 444 README.ms
        55  chmod 444 README.md
        56  ls -l scripts/deploy.sh
        57  ls -l backend/app/server.js
        58  ls -l README.md
        59  rm -r frontend/src/components
        60  cp -r backup/frontend/src/components frontend/src/
        61  rm -r temp
        62  rm -r temp/ <-Este comando no se ejecutó correctamente porque el directorio "temp" no existe.>
        63  ls
        64  rm backup/server_backup.js
        65  tree
        66  pwd
        67  history