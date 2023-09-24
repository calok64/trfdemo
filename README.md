# trfdemo

Directory structure
```bash
├── actions
│   ├── actions.py
│   ├── __init__.py
│   └── __pycache__
│       ├── actions.cpython-310.pyc
│       └── __init__.cpython-310.pyc
├── config.yml
├── credentials.yml
├── data (intents & actions for chatbot)
│   ├── nlu.yml
│   ├── rules.yml
│   └── stories.yml
├── deploy
│   ├── azure details
│   ├── config.tf
│   ├── configuration.tfrc.json
│   └── main.tf
├── diagrams (xml file(s) for diagrams to extract info and pass to chatgpt for generating script)
│   └── drawtest2.xml
├── domain.yml
├── endpoints.yml
├── flaskui
│   ├── chat.py
│   ├── gptscripts (scripts generated through chatgpt / openai)
│   │   ├── 1692381748_azurescripts.txt
│   ├── __pycache__
│   │   ├── chat.cpython-310.pyc
│   │   ├── imagetotext.cpython-310.pyc
│   │   └── xmltocode.cpython-310.pyc
│   ├── static (default folder for rasa chatbot to fetch templates and other assets)
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
│   ├── trfscripts (exported terraform scripts ready to deploy)
│   │   ├── 1694946965_azurescripts.tf
│   │   └── azure.tf
│   └── xmltocode.py ( extract information from xml file to create azure deployment scripts)
├── models
│   ├── 20230816-165126-avocado-bag.tar.gz
│   ├── 20230818-161405-hot-bounce.tar.gz
│   ├── 20230818-184931-excited-mirror.tar.gz
│   └── 20230819-002810-isomorphic-cathode.tar.gz
└── tests
    └── test_stories.yml

```
