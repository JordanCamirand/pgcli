## Jordan fork of PGCLI

This is a postgres client that does auto-completion and syntax highlighting.

Fork of: https://github.com/dbcli/pgcli/ which is an amazing project

### Main differences:
- Presetup all the DBs, their env and project path, so launching it is faster and smarter
- Have history be project based instead of global
- Output to JSON and open up in text editor / IDE of choice

### Setup:
- Using ASDF for python version management + Poetry for depedency management
- recommend adding an alias with something like

```
alias db='/Users/jordan/Library/Caches/pypoetry/virtualenvs/pgcli-QfguHkLv-py3.10/bin/python /Users/jordan/code/misc/pgcli/pgcli/main.py'
```
- You can see your python path with `poetry env info`, under the 'Virtualenv/executable'
- Create a config csv at: `~/.cust_db_cli_config.csv` like

```
project,env,db_url,path
web,local,<local_web_postgres_db_string>,/Users/jordan/code/web
web,dev,<dev_web_postgres_db_string>,/Users/jordan/code/web
catapult,local,<local_catapult_postgres_db_string>,/Users/jordan/code/catapult
```

Example if current working directory was `/Users/jordan/code/web` :

`db` to open up the CLI with <local_web_postgres_db_string>

`db --env=dev` to open up the CLI with <dev_web_postgres_db_string>

`db --project=catapult` to open up the CLI with <local_catapult_postgres_db_string>

### Configuration

update `EDITOR_COMMAND` in `pgcli/main.py` to be whatever editor you like ex: vim


### Misc

Format with: poetry run black .
