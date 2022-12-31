

```sh

mydnshostname=www.testserver.com

openssl req -x509 -newkey rsa:4096 -sha256 -days 3650 -nodes -keyout private.key -out certificate.cer -extensions san -config \
<(echo "[req]";
echo distinguished_name=req;
echo "[san]";
echo subjectAltName=DNS:localhost,DNS:$mydnshostname,DNS:$(hostname),IP:$(hostname -I | sed -e 's/\s*$//g' | sed -e 's/ /,IP:/g')
) -subj "/CN=genixidpserver"

openssl pkcs12 -export -in certificate.cer -inkey private.key -name sslcert -out keyStore.pfx  -password pass:certificatepassword


```