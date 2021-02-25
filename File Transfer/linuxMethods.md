# Linux File Transfer Methods

## Wget
```
wget [URL] -O [OUTPUT FILE]
```
## cURL
```
curl -o [OUTPUT FILE] [URL]
```
## NC
### Source Machine
```
nc -nvlp [PORT] > [OUTPUT FILE]
```
### Destination Machine
```
cat [FILE NAME] > /dev/tcp/[IP]/[PORT]
```
