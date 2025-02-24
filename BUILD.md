

# build docker images used for building linux binary
```bash
docker build -t svx_build .
````

# run 
```bash
docker run -it -v "$(pwd)"/svxlink/:/svxlink/ svx_build
```

# build
```bash
cd /svxlink/src/build
```

```bash
rm -rf * && cmake .. && make -j16
```

It will produce one sigle binary under
```bash
/svxlink/src/build/bin/svxreflector
```
