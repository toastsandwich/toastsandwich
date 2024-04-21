```
package main

import (
    "toastsandwich/introduction"
    "toastsandwich/skills"
    "toastsandwich/socials"
    "toastsandwich/work"
)

func introduce() {
    fmt.Println("Hello everyone, I am Shreyas Mali")
    fmt.Println("I am a GoLang Developer and a Competitve Programmer")
}

func currentWork() *work {
    fmt.Println(
    `Currently I am working on
    LCP - "Liver Cirrhosis Prediction System"
    which uses Random Forest Alogritm and Golang (Echo and Gorm)
    `
    )
    fmt.Println(
    `My previous projects are :
        1. Chat Server
        2. KeyLogger
        3. Database (still under build)
    `
    )
    return work                 
}

func connect() {
    connectWithMe := map[toastsandwich.socials]string {
		Instagram: "this.shrys",
		LinkedIn: 	"Shreyas Mali",
    }
	fmt.Println(connectWithMe)
}

func main() {
	introduct()
	currentWork()
	connect()
}
```
