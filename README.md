## Commands
### Run docker container
`docker build -t my-golang .`
`docker run -p 8080:8080 my-golang`

## Build go binary for different systems
`GOOS=linux go build` Builds go for linux

## Check what system the binary was built for
`file the_binary_name_here`
Example: `file go-server`
Output: Mac go-server: Mach-O 64-bit executable x86_64

## Log into cf container
`cf ssh the_container_name_here`
Example: `cf ssh go-server`


## TROUBLESHOOTING
### P Dubs token revoked
`cf push`
Output: Pushing from manifest to org tbartlett-go-docker / space development as tbartlett@pivotal.io...
Using manifest file /Users/tamarabartlett/Dev/go/src/github.com/tamarabartlett/go-server/manifest.yml
Getting app info...
Error: The token expired, was revoked, or the token ID is incorrect. Please log back in to re-authenticate.`

How to fix: Run `cf login`
