|Build Status| |CodeCov| |PyPI| |netlify|

This is a postgres client that does auto-completion and syntax highlighting.

Fork of: https://github.com/dbcli/pgcli/ which is an amazing project

***Main differences:
- Presetup all the DBs, their env and project path, so launching it is faster and smarter
- Have history be project based instead of global
- Output to JSON and open up in text editor / IDE of choice

Setup:
- Using ASDF for python version management + Poetry for depedency management
- recommend adding an alias with something like
alias db='/Users/jordan/Library/Caches/pypoetry/virtualenvs/pgcli-QfguHkLv-py3.10/bin/python /Users/jordan/code/misc/pgcli/pgcli/main.py'
- You can see your python path with poetry env info, under the 'Virtualenv/executable'

Format with: poetry run black .
