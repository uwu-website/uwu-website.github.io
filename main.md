
# UwU - Universal Web Utility

UwU is a tool that was made to make web apps security testing more easy.

It's idea was `just run and chill waiting for results`.

UwU itself is a plugin engine and it's very easy to write plugins for it.

It also offers many pre-installed plugins that are suitable for basic testing (or CTF) tasks.

Example will be listed down below.

# Installing

### Using install.sh script
    bash install.sh
### Manually (with sudo):
    mkdir /usr/share/UwU/plugins/
    g++ -o main main.cpp -ldl
    cp ./main /bin/uwu

# Writing plugins

As i said previously is's easy to write plugins for UwU.

Here is the example:

    #include <iostream>
    #include <string>
    #include <cpr/cpr.h>

    #include <UwU/defs.cpp>

    using namespace std;

    extern "C" 
    {
        int plugin_start(string url, string protocol, map<string, string> postparams) 
        {
            cout << INFO << "Hello from my plugin!" << endl;
            return 0;
        }
    }

# Authors

- [`@TryH4ckM3`](https://www.github.com/Try-H4ck-M3)
- [`@Andrey-oss`](https://github.com/Andrey-oss)
