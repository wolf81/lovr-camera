# LÖVR Camera

A camera module for [LÖVR](https://lovr.org) based on the [FPS Controls](https://lovr.org/docs/Flatscreen/FPS_Controls) example code.

```bash
% git submodule init
% git submodule update
```

# Usage

See the included `main.lua` file for a working example, but in short:

```lua
-- import camera module
local Camera = require 'Camera'

-- create new instance
local camera = Camera()

function lovr.load(args)
    -- configure camera, this will allow mouse turning
    camera:init()
end

function lovr.update(dt)
    -- update camera transform based on speed, time
    camera:update(dt)
end

function lovr.draw(pass)
    -- draw using the camera
    camera:draw(pass, function() 
      -- do additional drawing here 
    end)
end
```
