# RoduxWatcher

Inspired by `Silo:Watch()`. https://sleitnick.github.io/RbxUtil/api/Silo/#Watch

Usage is similar.

```lua
local RoduxWatcher = require(path.to.module)

local watcher = RoduxWatcher(State)

local disconnect = watcher(function(state)
	return state.Statistics.Points
end, function(points)
	print("Points", points)
end)

-- To stop watching, just call disconnect:
disconnect()
```