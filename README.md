```go
package main

import (
    "fmt"
    "toastsandwich/experience"
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
    work.Add <- `Currently working on: Completing my degree :_)`
    work.Done <- struct{}{} // Signal that the current work is done

    work.Add <- `Previous Projects:
        1. KeyLogger                  [stack : C++ and NodeJS]
        2. ChatServer                 [stack : Golang]
        3. Database from scratch      [stack : Golang] {work in progress}
        4. LCP                        [stack: HTML, CSS, JS, Golang]
        5. toastsandwich.snippet.box  [stack: "HTML, CSS, GOHTML, Golang]`
    work.Done <- struct{}{} // Signal that the project list is done
}

func connect() {
    connectWithMe := map[string]string {
        "Instagram": "this.shrys",
        "LinkedIn":  "Shreyas Mali",
    }
    fmt.Println(connectWithMe)
}

func init() {
    experience.Load("intern @TSYS")
    skills.Load("golang", "templ", "react", "html", "css", "mysql", "docker")
}

func main() {
    introduce()

    // Start working in a goroutine
    go currentWork()

    // Wait for the work to be done before proceeding
    <-work.Done

    // After the work is done, proceed to connect
    connect()
}

```
