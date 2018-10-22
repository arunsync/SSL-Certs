# SSL-Certs

If the website/server has the SSL certificates, follow the steps below to download them. Only root cert is enough to make SSL communication secure.
  1. From Windows
      -> launch the webstie in the browser and download the certs 
  2. From Linux
      -> openssl s_client -connect {HOSTNAME}:{PORT} -showcerts
      this will show the certs in txt format, we have to store it with the name specified in the response and save it in .crt file.
      
After downloading the cert, import the certs in to java truststore (cacerts) which is inside jre/lib/security


Self Signed certificate
  A self signed certificate will still encrypt the communication between the client (browser) and your server.

