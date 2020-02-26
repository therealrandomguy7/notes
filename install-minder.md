### Installing Minder in Lubuntu
- [git clone](https://github.com/phase1geo/Minder)
- build app
***
While running `./app run` for the build, there is the aforementioned error.
I'm running __Lubuntu 19.10__
Details:
```
$ ./app run
.....
.....
[144/144] Linking target com.github.phase1geo.minder.

(com.github.phase1geo.minder:18128): GLib-GIO-ERROR **: 11:10:09.244: Settings schema 'com.github.phase1geo.minder' is not installed
./app: line 44: 18128 Trace/breakpoint trap   (core dumped) ./com.github.phase1geo.minder "${@:2}"
```

After __searching online__ (links: [1](https://github.com/phw/peek/issues/344), [2](https://stackoverflow.com/a/28953973)), and trying out various approaches, this is what I have found out:
* in Lubuntu, by default, there is __NO__ `/usr/local/share/glib-2.0/schemas/` directory, <br>so had to manually create `glib-2.0/schemas` directories inside `/usr/local/share/`

* after a clean build, `com.github.phase1geo.minder.gschema.xml` was copied to `/usr/local/share/glib-2.0/schemas/` <br>but **was not compiled** to `gschemas.compiled`
* initially, i manually compiled the `com.github.phase1geo.minder.gschema.xml` inside `.../Minder/data/` <br>using <br>`glib-compile-schemas .../Minder/data/`<br>but, this did not solve the error
* after manually compiling the schema inside `/usr/local/share/glib-2.0/schemas/`, and a clean & rebuild, the build was a success!

I have successfully solved the issue on my system through hit & trial, without any knowledge of the finer details. 
__Is this issue a bug, or is it an isolated issue?__
Please take steps accordingly. 

***
- success build, then install 
- accompanying [minder file](/minder/Minder-Install.minder)