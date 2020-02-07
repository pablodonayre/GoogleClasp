# GoogleClasp
Ubuntu 16.04 image with CLASP 2.1.0


### INSTRUCTIONS:

1) Clone this public repository: git clone https://github.com/pablodonayre/GoogleClasp.git

2) Go inside CLASP directory

3) Execute the following commands (Need to be at the level of docker-compose.yml):

    `docker-compose up -d`

4) At this point, the container should be running, check them with: 

    `docker ps -a`

5) In the host machine. Login to your Google Account

6) In the host machine. Enable Google Apps Script API: https://script.google.com/u/1/home/usersettings

7) Go Inside the container: 

    `docker exec -it {container name} bash`

8) Inside the container execute (Login to your account): 

    `clasp login [--no-localhost]`

9) Inside the container execute (to clone a project): 

    `clasp clone {Project ID}`

Example:
    The URL of a Google Apps Script Project is like:
    https://script.google.com/d/1sjfQvLeCcNAtaDSAdZMF_6HFAIQYwnfdobkw8D9lsAxrI8jb9B3sXV2Y/edit?usp=drive_web

    So the ID of the project is:
    1sjfQvLeCcNAtaDSAdZMF_6HFAIQYwnfdobkw8D9lsAxrI8jb9B3sXV2Y

------------------------------------------------------------------------------------------------
### CLASP COMMANDS:

`clasp login [--no-localhost] [--creds <file>]`

`clasp logout`

`clasp create [--title <title>] [--type <type>] [--rootDir <dir>] [--parentId <id>]`

`clasp clone <scriptId | scriptURL> [versionNumber] [--rootDir <dir>]`

clasp pull [--versionNumber]

clasp push [--watch] [--force]

clasp status [--json]

clasp open [scriptId] [--webapp] [--creds]

clasp deployments

clasp deploy [--versionNumber <version>] [--description <description>] [--deploymentId <id>]

clasp undeploy [deploymentId] [--all]

clasp version [description]

clasp versions

clasp list
