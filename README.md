# go-strip-markdown
A Markdown stripper written in Go (golang).

## Usage
You could create a simple command-line utility:

```go
package main

import stripmd "github.com/writeas/go-strip-markdown"
import "fmt"
import "os"

func main() {
	if len(os.Args) < 2 {
		os.Exit(1)
	}
	fmt.Println(stripmd.Strip(os.Args[1]))
}
```

You could pass it Markdown and get pure, beauteous text in return:

```bash
./strip "# A Tale of Text Formatting

_One fateful day_ a developer was presented with [Markdown](https://daringfireball.net/projects/markdown/).
And they wanted **none of it**."

# A Tale of Text Formatting
#
# One fateful day a developer was presented with Markdown.
# And they wanted none of it.
```

## Inspiration
This was largely based off of [remove-markdown](https://github.com/stiang/remove-markdown), a Markdown stripper written in Javascript.

## License
MIT.
