# Site

I've done this simple site using emscripten

The main.wasm file is a binary fail supoported by every browser.

The js file is not an instruction script trying to recreate C, it has a particular structure for understanding that WASM code.

This way we can get a website coding it only in C.

# Run site

For running the site you can just run a http.server using any service. Python can be used:
```
python3 -m http.server --bind 127.0.0.1 8000
```

# Screenshoots

![image](https://user-images.githubusercontent.com/84512017/172051122-9bcf8b1f-8231-4fd2-ab2c-d1dba05fd40c.png)

![image](https://user-images.githubusercontent.com/84512017/172051132-8ba2823b-65d6-49c8-ab10-c8331c765fca.png)

# Create your own!

You can just create a simple C file:
```c
#include <stdio.h>

int main()
{
  printf("Hello, World!");
  return 0;
}
```
And run this commands:

```
emcc main.c -o index.html
emcc main.c -o index.js
```

If you dont have emcc installed:
```
sudo apt install emscripten
```
