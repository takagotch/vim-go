### vim-go
---
https://github.com/fatih/vim-go

```go
// test/parse.go
package html

import (
)

func (p *parser) addText(text string) {
  if text == "" {
    return
  }
  
  if p.shouldFosterParent() {
    p.fosterParent(&Node{
      Type: TextNode,
      Data: text,
    })
    return
  }
  
  t := p.top()
  if n := t.LastChild; n != nil && n.Type == TextNode {
    n.Data += text
    return
  }
  p.addChild(&Node{
    Type: TextNode,
    Data: text,
  })
}













```

```
```

```
```


