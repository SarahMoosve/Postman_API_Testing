# Postman_API_Testing


## Project Structure
- `postman_collection.json`: It carries the collection of a simple book API
        - It handles the following requests.
          -API status
          -Token
          -Get all books
          -Get a single book
          -Submit book order
          -Get all books orders
          -Update an order
          -Get one order
          -Delete order

- `workspace.postman_globals.json`: Contains global variables.
        - It defines:
          -`{{baseUrl}}`: 
                    https://simple-books-api.glitch.me
          -`{{bookId}}`: dynalically generated
          -`{{singleBookId}}`: dynalically generated
          -`{{SubmitOrderId}}`: dynalically generated
          -
- `workspace.postman_globals.json`: Inside a newman folder, this is the html report of the collection.


## Setup & Installation
1. Clone the Repository:

git clone https://github.com/yourUsername/Cypress_Practice_Projects.git
cd Cypress_Practice_Projects
2. Install postman.
3. Open `postman_collection.json` inside Postman.
4. Add the global environments from `workspace.postman_globals.json` in the environments
5. Open runner and drag this folder inside the runner to run all the requests in a single go.

6. To install newman, use the following commands:
        - Install node.js and npm

```bash
        sudo apt update
        sudo apt install nodejs npm
```

        - Verify if installed

```bash
        node -v
        npm -v
```

-Install newman
```bash
        sudo npm install -g newman
        newman -v
```
        7. Install Newman HTML Reportor:

```bash
        npm install -g newman-reporter-htmlextra 
```

```bash
        npm install -g newman-reporter-htmlextra
```
        - After installation is completed, execute the following to generate report.
```bash
        newman run `postman_collection.json` -g `workspace.postman_globals.json` --reporters cli,htmlextra
```

Now, go to the newman folder, click on the `.html` file to run it




