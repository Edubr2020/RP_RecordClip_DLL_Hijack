Remote DLL Hijack Vulnerability in Real Player 

The Player application and the Recording Manager are prone to a remote DLL hijack (binary planting) issue because of unsafe search for unexisting DLLs.
To exploit the issue attackers would have to convince the target to open a media file from a WebDAV or SMB share.

For Real Player prior to V.20.1.0.312:

edit the RAM file and the HTML file and replace "%server%" with the actual server host name or IP
"%share%" with actual share name. Target needs to open the RAM file that also invokes the HTML file with code to invoke Recording Manager app and the DLL is loaded instantly and code runs from the "DLLMain()" function.

For RP V.20.1.0.312:

Just edit the RAM file 'start_RP_V.20.1.0.312.ram' and replace "%server%" with the actual server host name or IP
"%share%" with actual share name. When the target opens the RAM file, needs to wait a little while until the DLL is loaded.


dll names: pnrs3260.dll
	   mediautil.dll





