# Crearlo


```
USERNAME=jganzabal

IMAGE_NAME=$USERNAME/ml-basic-tools:latest

docker build -t $IMAGE_NAME .
```

# Probarlo

```
docker run -it $IMAGE_NAME /bin/bash
```

# Verificar que funciona
```
root@d4a6c5fa4f79:/# python
Python 3.11.3 (main, May 23 2023, 13:51:55) [GCC 8.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import pandas as pd
>>> exit()
root@d4a6c5fa4f79:/# exit
exit
```


# Pushearlo
Tener en cuenta que tiene que cambiar el `USERNAME` de la imagen con su usuario y estar logueado
https://docs.docker.com/engine/reference/commandline/login/

```
docker push $IMAGE_NAME
```
