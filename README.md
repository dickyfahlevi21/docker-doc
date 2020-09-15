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
```python
FROM nginx:alpine
COPY . /usr/share/nginx/html
```
setelah itu CTRL X, lalu pilih Yes(Y)
