Custom class library for lua, similar usage to python classes.

# Example Usage:
```lua
require("class")
local superClass = class {
  init = function(self, val)
    self.val = val  
  end,

  printVal = function(self)
    print(self.val)
  end
  }

local Sub = class(superClass, {
  init = function(self, val)
    superClass.init(self, val)
  end,
  })

local sub1 = Sub:new(10)
sub1:printVal()
```
