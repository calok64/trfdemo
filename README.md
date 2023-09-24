# trfdemo
**About Project**
This is a POC for deploying converting diagram to code and generating terraform deployment scripts using azure. The flask ui helps to interact with rasa chatbot with chatgpt as backend to generate scripts and edit them before deploying to azure cloud using terraform cli.

**Main directory :** rasademo
**Directory structure**
```bash
├── actions
│   ├── actions.py
│   ├── __init__.py
│   └── __pycache__
│       ├── actions.cpython-310.pyc
│       └── __init__.cpython-310.pyc
├── config.yml
├── credentials.yml
├── data # intents & actions for chatbot
│   ├── nlu.yml
│   ├── rules.yml
│   └── stories.yml
├── deploy
│   ├── azure details
│   ├── config.tf
│   ├── configuration.tfrc.json
│   └── main.tf
├── diagrams # xml file(s) for diagrams to extract info and pass to chatgpt for generating script. Your diagram xml file will be copied to this directory.
│   └── drawtest2.xml
├── domain.yml
├── endpoints.yml
├── flaskui
│   ├── chat.py
│   ├── gptscripts # scripts generated through chatgpt / openai
│   │   ├── 1692381748_azurescripts.txt
│   ├── __pycache__
│   │   ├── chat.cpython-310.pyc
│   │   ├── imagetotext.cpython-310.pyc
│   │   └── xmltocode.cpython-310.pyc
│   ├── static # default folder for rasa chatbot to fetch templates and other assets
│   │   └── assets
│   │       ├── brand
│   │       │   ├── bootstrap-logo.svg
│   │       │   └── bootstrap-logo-white.svg
│   │       ├── css
│   │       │   └── styles.css
│   │       ├── dashboard.css
│   │       ├── dashboard.js
│   │       ├── dashboard.rtl.css
│   │       ├── dist
│   │       │   ├── css
│   │       │   │   ├── bootstrap.min.css
│   │       │   │   ├── bootstrap.min.css.map
│   │       │   │   ├── bootstrap.rtl.min.css
│   │       │   │   └── bootstrap.rtl.min.css.map
│   │       │   └── js
│   │       │       ├── bootstrap.bundle.min.js
│   │       │       └── bootstrap.bundle.min.js.map
│   │       ├── jquery.min.js
│   │       └── js
│   │           └── scripts.js
│   ├── templates
│   │   ├── editscript.html
│   │   ├── index.html
│   │   ├── myfolder.html
│   │   └── trfscripts.html
│   ├── trfscripts # exported terraform scripts ready to deploy. Check the file properly for each parameter before converting into .tf file
│   │   ├── 1694946965_azurescripts.tf
│   │   └── azure.tf
│   └── xmltocode.py # extract information from xml file to create azure deployment scripts
├── models
│   ├── 20230816-165126-avocado-bag.tar.gz
│   ├── 20230818-161405-hot-bounce.tar.gz
│   ├── 20230818-184931-excited-mirror.tar.gz
│   └── 20230819-002810-isomorphic-cathode.tar.gz
└── tests
    └── test_stories.yml

```
**Infrasctructure:**
1) [VirtualBox for Windows](https://www.virtualbox.org/wiki/Downloads)
2) [LinuxMint 21 Cinnamon 64Bit](https://www.linuxmint.com/download.php)
3) Linux VM 35GB with 12GB RAM
4) [Terraform Cloud](https://app.terraform.io/public/signup/account)
5) [Azure Free Trial Account](https://azure.microsoft.com/en-in/free)
6) IDE used [Visual Studio Code](https://code.visualstudio.com/)
7) For diagrams [draw.io](https://draw.io/)
   
**Setting up the project :**
1) [Create a python virtual environment (venv)](https://docs.python.org/3/library/venv.html)
2) Activate virtual environment - $ source venv/bin/activate
3) Install packages - pip install -r requirements.txt
   ( You can refer below links for installing rasa and flask if you want to understand more )
4) [Install Rasa on Ubuntu](https://learning.rasa.com/installation/ubuntu/)
5) [Install Flask on Ubuntu](https://linuxize.com/post/how-to-install-flask-on-ubuntu-20-04/)
6) [Setting up Terraform on Linux VM (Ubuntu) for Azure](https://developer.hashicorp.com/terraform/tutorials/azure-get-started)
   
**Runnning the project :**
1) Activate venv
2) Start rasa server => rasa run -m models --enable-api
3) Train rasa model => rasa train
4) Start Flask server => flask --app chat run 

