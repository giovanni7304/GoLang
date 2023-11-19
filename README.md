#README
Go Language Example
Be sure to have Docker and Go loaded before starting this example.
let's create a new module in our VSCode folder for this application.
VSC>go mod init container-go-app
The previous command created go.mod
VSC>touch main.go
VSC>go run main.go
VSC>touch dockerfile
VSC>docker build . -t go-container:latest
VSC>docker image ls | grep go
VSC>docker run go-container:latest
Hello World

Let's build a new main.go that will actualy discplay on a web browser
Let's get the code from github
VSC>go get -u github.com/gin-gonic/gin
Wait for it to download.
It will create a new file called 'go.sum'
VSC>docker build . -t go-container_app:latest
then go to the "tests.http" file and click "send request"
Make sure you get the "pong" echo
VSC>docker run -e PORT=9000 -p 9000:9000 go-container_app:latest
