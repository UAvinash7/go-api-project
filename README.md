GO-API's Using Gin Framework

Create a go mod file using `go mod init` command followed by project folder name.

Download the gin framework dependency using `go get` command and it will install the gin framework.
i.e., `go get github.com/gin-gonic/gin`

Here we are creating a kind of library api where we are going to store a bunch of books, check-in a book, check-out a book, add books, view all the different book availability, get a book by its id.

To accomplish it, we need to write different functions like getBook, createBook, bookById, checkoutBook, returnBook and helper function like getBookById and routes like GET, POST, PATCH and Run that we can have for our api's.

Run the program by using `go run main.go` command and hit the above mentioned routes using curl command or postman tool or browser like
`localhost:8080/books`, 
Add a new book structure inside of body.json file and hit the following command
`localhost:8080/books --include --header "Content-Type: application/json" -d @body.json --request "POST"`
Now to  cross check if the book is added successfully or not use
`localhost:8080/books`
Checkout functionality
`localhost:8080/checkout?id=2 --request "PATCH"`
Return book functionality
`localhost:808/return?id=2 --request "PATCH"`



