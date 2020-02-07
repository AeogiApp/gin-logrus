# gin-logrus

[Logrus](https://github.com/Sirupsen/logrus) logger middleware for [Gin](https://github.com/gin-gonic/gin), based on [gin-logrus](https://github.com/toorop/gin-logrus).

## Usage
```go
package main

import (
	"github.com/AeogiApp/gin-logrus"
	"github.com/gin-gonic/gin"
	"github.com/sirupsen/logrus"
)

func main() {
    log := logrus.New()
    
    r := gin.New()
    r.Use(ginlogrus.Logger(log))
    
    
    r.GET("/ping", func(c *gin.Context) {
        c.Data(200, "text/plain", []byte("pong"))
    })
    
    r.Run(":8080")
}
```
