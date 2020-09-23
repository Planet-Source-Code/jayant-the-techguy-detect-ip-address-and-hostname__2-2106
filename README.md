<div align="center">

## Detect IP address and hostname


</div>

### Description

Detect IP address and hostname
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Jayant The TechGuy](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/jayant-the-techguy.md)
**Level**          |Intermediate
**User Rating**    |4.0 (16 globes from 4 users)
**Compatibility**  |
**Category**       |[Internet/ Browsers/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-browsers-html__2-68.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/jayant-the-techguy-detect-ip-address-and-hostname__2-2106/archive/master.zip)





### Source Code

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">
<html>
<head>
	<title>Detect IP address and hostname</title>
</head>
<body>
<BODY>
<!-- Script by Jayant Kumar Gandhi - www.jayantgandhi.com -->
<SCRIPT LANGUAGE="JavaScript">
<!-- Begin
// detect whether IE or netscape
netscapeTest = parseInt(navigator.appVersion)
explorerTest = navigator.appName.indexOf("Microsoft") + 1
// detect hostname for Netscape 3
function netscapeThree() {
if (navigator.javaEnabled()) {
userDomain = java.net.InetAddress.getLocalHostName()
return (userDomain.toString())
} else {
return null
  }
}
// detect hostname and IP address for Netscape 4
// Note here baseaddress is in format 'hostname/ip-address'
// getHostName() gets us the host name
function netscapeFour() {
if (navigator.javaEnabled()) {
baseAddress = java.net.InetAddress.getLocalHost()
userDomain = baseAddress.getHostName()
return (userDomain.toString())
} else {
return null
  }
}
if ((explorerTest == "0") && (netscapeTest == "3")) {
domainName = netscapeThree()
}
else if ((explorerTest == "0") && (netscapeTest == "4")) {
domainName = netscapeFour()
}
else {
domainName = "Domain name can be detected only on Netscape and compatible browsers. <br>Internet Explorer users must use Netscape to see the actual result"
}
document.write(domainName)
// End -->
</SCRIPT>
</body>
</html>
```

