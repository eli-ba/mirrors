# Create mirrors for Git repositories

## Create a `mirrors.json` file under `~/myproject`
```json
{
	"primary": "https://github.com/myusername/myproject.git",
	"mirrors": [
		"https://myusername@bitbucket.org/myusername/myproject-mirror1.git",
		"https://myusername@bitbucket.org/myusername/myproject-mirror2.git"
	]
}
```
The `primary` URL will be push+fetch, the `mirrors` URLs will be fetch only.

## Run with Docker
```shell script
cd ~/myproject
docker run --rm -it -v "$PWD":/work eliba1/mirrors
```
