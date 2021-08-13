# Svelte.js + Flask + Heroku Starter
The demo lives at https://github.com/y330/Flask-Svelte-Heroku-starter
##  [Yonah Aviv](https://yonah.ml)
Flask with support for Svelte Single Page applications(SPA), and easy deployment to heroku. Anything other than svelte may require you to change the of inside the client folder. Make sure the client folder looks something like this(or make sure webpack or rollup or snowpack builds your source files to result in the following)

```
client/
	public/
		build/
			bundle.css
			bundle.js
		index.html
		...
	...
...
```
The client folder is just the official svelte starter with a couple of modifications.

this repo is based on a medium article and a github repository


Features:
- Python 3.9
- Flask 2.0
- Pipenv [Pipfile](Pipfile)
- Heroku integration for easy deployment [Procfile](Procfile)
- Svelte(SPA) in the [client/](client/) folder.
- rollup


If there is a .venv folder in project root directory, Pipenv will create a local environment instead of a global one.


I suggest you use two seperate terminal tabs(one for root, one for client). to do this in VScode, press
```
ctrl+` for terminal

ctrl+shift+5 for a new terminal beside the original one

in the new terminal:
cd client

and then your done
terminal 1 = flask(root dir)
terminal 2 = svelte(client dir)


````
```bash
	# Terminal 1
	pipenv install
	#==start dev==
	flask run


	# Terminal 2
	pnpm i

	#==start dev==
	pnpm run dev


```

### Deploy
publish project to github
1. open heroku
2. create new app
3. connect with github
4. and press deploy

-------------------------------
// From original repo(ignore) didnt work for me so i modified the repo

A super simple example of using Flask to serve a Svelte app and use it as a backend server.

Run the following for development:

- `python server.py` to start the Flask server.
- `cd client; npm install; npm run autobuild` to automatically build and reload the Svelte frontend when it's changed.

This example just queries the Flask server for a random number.
