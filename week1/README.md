# **Task Management using Raft Consensus**

## Initilation 

### Creating virtual environment

```bash
python -m venv venv
venv/Scripts/activate #only for win
```

### Installing modules

```bash
pip install -r requirements.txt
```

### DB init



In `node.py` make changes to this line according to your configuration.
```bash
self.mydb = mysql.connector.connect(host="localhost", user="root",password="password123", database="task")
```

Make sure that the database is already created with the name `task`. Also the tables,`users` and `tasks`, also need to be made before running the code 

- Creating db
```bash
drop database task;
create database task;
use task;
```

- Creating table
```bash

```

### To run servers

- Terminal 1
```bash
python server.py 0 ip_list.txt
```

- Terminal 2
```bash
python server.py 1 ip_list.txt
```

- Terminal 3
```bash
python server.py 2 ip_list.txt
```

- Terminal 4
```bash
python server.py 3 ip_list.txt
```

- Terminal 5
```bash
python server.py 4 ip_list.txt
```

- Terminal 6
```bash
streamlit run app.py
```