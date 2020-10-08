# login-page-swarm
Login Page For Swarm


Libraries Used: urlparse, http (cookies, HTTPServer, HTTPRequestHandler)


BaseHTTPRequestHandler
- path (url)
- 


Route Handlers:

Get: 
if url starts with "/login":
  if "X-Target" header is not there, send 500 response code 
  extract target from header,  write byte-encoded html string of auth form with target given

html signup form form as string
else send 200 response code and a byte-encoded string saying hello


Post:
Read the form concent (from rfile, headers)
extract required fields
if present:
  send response 302
  send header "Set-Cookie" with nginx auth key and value which is byte encoded
