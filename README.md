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
    fmt.Println("I am a GoLang Developer and a Competitive Programmer")
}

func currentWork() {             
	work.add <- 	`Currently working on :
			Liver Cirrosis Prediction System using Random Forest as a web application [stack : Golang, HTML, CSS]`
	work.done <- struct{}{}
	work.add <-	`Previous Projects :
			 1. KeyLogger             [stack : C++ and NodeJS]
			 2. ChatServer 		  [stack : Golang]
			 3. Database from scratch [stack : Golang] {incomplete}`
	work.done <- struct{}{}
}

func connect() {
    connectWithMe := map[socials.links]string {
		Instagram: "this.shrys",
		LinkedIn:  "Shreyas Mali",
    }
	fmt.Println(connectWithMe)
}

func main() {
	introduct()
	for {
		select <-work.done {
		case true:
		// go to next work
		case false:
		// do work until complete
		}
	}
	connect()
}
```
