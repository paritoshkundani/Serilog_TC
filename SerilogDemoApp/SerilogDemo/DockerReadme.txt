docker run -d --restart unless-stopped --name seq -e ACCEPT_EULA=Y -v C:\work\proj\Serilog_TC\SerilogDemoApp\SerilogDemo\Logs:/data -p 8081:80 datalust/seq:latest

use above command to get seq setup with docket.

-d means dettached mode, we can shut powershell command prompt and it will continue running the image
--restart unless-stopped means if image crashes it should restart unless we force it to stop
--name seq means give image the name "seq"
-e ACCEPT_EULA = Y the -e is to setup an environment variable, here we agree to the EULA
-v path:/data means path the path on local machine to the /data path in image
-p is to map localport 8081 to port 80 in image
datalust seq:/latest means get the latest version of seq if we don't have it already, if there will just run existing, else get and run it


to list images use command:
docker images