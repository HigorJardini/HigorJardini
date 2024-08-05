<p align="left">

  [![Linkedin: thaianebraga](https://img.shields.io/badge/-higorjardini-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/higorjardini/?locale=en_US)](https://www.linkedin.com/in/higorjardini/?locale=en_US)
  [![Twitter: ThaiiBraga](https://img.shields.io/twitter/follow/higor_jardini?style=social)](https://twitter.com/higor_jardini)
  [![GitHub Thaiane](https://img.shields.io/github/followers/HigorJardini?label=follow&style=social)](https://github.com/HigorJardini)

</p>

<a target="_blank" href="https://higorjardini.dev/"><img src="https://github.com/HigorJardini/HigorJardini/blob/main/higorjardini.dev.png?raw=true" alt="higorjardini.dev macbook image" min-width="300px" max-width="300px" width="300px" align="right"></a>

```go
// Hi, I'm Higor Jardini!
package main

import (
    "fmt"
    "net/http"
)

// SoftwareEngineer holds my profile info
type SoftwareEngineer struct {
    Name          string   // Name
    Backend       bool     // Backend expertise
    Frontend      bool     // Frontend skills
    PortfolioLink string   // Portfolio link
    Skills        []string // Technical skills
}

func main() {
    engineer := SoftwareEngineer{
        Name:          "Higor Jardini",
        Backend:       true,
        Frontend:      false,
        PortfolioLink: "https://higorjardini.dev/",
        Skills:        []string{"Go", "Node.js", "Java", "TypeScript"},
    }

    http.HandleFunc("/", func(w http.ResponseWriter, r *http.Request) {
        fmt.Fprintf(w, "Hi, I'm %s!\n", engineer.Name)
        fmt.Fprintf(w, "Backend development with skills in %v.\n", engineer.Skills)
        fmt.Fprintf(w, "Visit my portfolio at %s.", engineer.PortfolioLink)
    })

    http.ListenAndServe(":8080", nil)
}
```

##

![Snake animation](https://github.com/HigorJardini/Higorjardini/blob/output/github-contribution-grid-snake.svg)

