# DOCKER DOCUMENTATION

1. Buat folder
```bash
mkdir testbuatdocker
```

2. Masuk ke foldernya
```bash
cd testbuatdocker
```

3. Buat Dockerfile
```bash
nano Dockerfile
```
input code berikut untuk menggunakan NGINX
```Dockerfile
FROM nginx:alpine
COPY . /usr/share/nginx/html
```
setelah itu CTRL X, lalu pilih (Y)Yes

4. Buat index.html

```bash
nano index.html
```

masukan contoh tag html
```HTML
<p>Docker Pertamaku</p>
```

5. Docker build image

```bash
docker build -t dockerpertamaku:v1
```

6. Docker Create Container

```bash
docker container run -d -p 1111:80 --name pertama dockerpertamaku:v1
```

lalu cek url docker kalian pada browser
```bash
http://0.0.0.0:1111/
```


7. Cek images dan tag image nya
```bash
docker images
```

ouputnya:
```bash
REPOSITORY              TAG       IMAGE ID         CREATED           SIZE
dockerpertamaku         v1        023ab91c6291     3 minutes ago     1 MB
```

command tag
```bash
docker tag 023ab91c6291 dickyfahlevi21/dockerpertamaku:v1
```

8. Push image nya
```bash
docker push dickyfahlevi21/dockerpertamaku
```