## Preview <br/>
![Preview](https://github.com/dev-luciolins/mta-slidebar/blob/main/slidebar.png)

## Installation
To use this Slidebar utility, include the Lua file in your MTA:SA project and load the file in meta.xml.

Example `meta.xml` entry:
```xml
<script src = 'path/slidebar.lua' type = 'client' cache = 'false' />
```

# Functions
Creating a slidebar
```lua
slidebar = Slidebar:Create (
    { -- Positions
        x = float, -- X coordinate of the top left corner of the image
        y = float, -- Y coordinate of the top left corner of the image
        w = float, -- width
        h = float, -- height
        circle = {
            w = float, -- width of the circle (It is ideal that the number is equal)
            h = float, -- height of the circle (It is ideal that the number is equal)
        },
    },
    { -- Colors
        background = int, -- Background color of the slidebar (tocolor)
        progress = int, -- Progress color of the slidebar (tocolor)
        circle = int, -- Circle color of the slidebar (tocolor)
    },
    { -- definitions
        minimum = int, -- The min value of the slidebar
        maximum = int, -- The max value of the slidebar
        defaultValue = int, -- Default value of the slidebar
    }
);
```

## Rendering the slidebar
### Syntax
```lua
slidebar:render ()
```
### Returns
* Returns nil

## Changing the value of slidebar
### Syntax
```lua
slidebar:setValue (int value)
```
### Returns
* Returns true if successful, an error message otherwise.

## Getting the value of slidebar
```lua
slidebar:getValue ()
```
### Returns
* Returns number

## The click Function
### Syntax
```lua
slidebar:click (string button, string state, float absoluteX, float absoluteY)
```
### Returns
* Returns true if successful, an error message otherwise.

## Contributing
Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request with a clear description of the changes you’ve made.

Ensure that your code follows the project's style guidelines and is well-tested.

## License
This library is released under the MIT License. See the [LICENSE](https://github.com/dev-luciolins/mta-slidebar/blob/main/MIT-LICENSE.txt) file for details.

## License Summary
You can use, modify, and distribute this library freely, provided that all copies include the original copyright notice and license. The library is provided "as-is", without warranty of any kind.