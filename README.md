# swagno-gin
gin-gonic middleware to serve Swagger Ui files and doc.json file which generated from [Swagno](https://github.com/go-swagno/swagno)

## Usage

1. Get [Swagno](https://github.com/go-swagno/swagno)
2. Create your endpoint array. See: https://github.com/go-swagno/swagno/blob/master/README.md#getting-started
3. Get swagno-gin
```sh
go get github.com/go-swagno/swagno-gin
```
4. Import swagno-gin to your handler
```go
import "github.com/go-swagno/swagno-gin/swagger"
```
5. **Be sure you created swagger instance and endpoints**
6. Create swagger handler
```go
a.GET("/swagger/*any", swagger.SwaggerHandler(sw.GenerateDocs()))
```
7. Visit /swagger and /swagger/doc.json for confirmation
