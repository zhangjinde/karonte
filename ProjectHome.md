What is a **"Managed File Transfer"** ?

An organization for having a "Managed File Transfer" needs to configure, track and audit a file transfer in a consistent way.
The requirements for a "Managed File Transfer" are:

  * Audidatibility
  * Ease-of-use
  * Simplicity
  * Security
  * Recoverability
  * Reliability
  * Platform connectivity
  * Automation

It exists some payment tools:
  * [IBM-Sterling Connect:Direct](http://www-01.ibm.com/software/commerce/managed-file-transfer/products/connect-direct/)
  * [IBM Websphere MQ FTE](http://www-01.ibm.com/software/integration/wmq/filetransfer/)
  * [Axway SecureTransport](http://www.axway.com/products-solutions/mft/gateways/securetransport)
  * [Primeur MFT/S](http://www.primeur.com/mft-soluzioni-managed-file-transfer)
  * [Stonebranch](http://www.stonebranch.com/solutions/file-and-ftp-management-and-transfer/)
  * [GoAnywhere Director™](http://www.goanywheremft.com/solutions/managed-file-transfer)
  * [Ipswitch File Transfer](http://www.ipswitchft.com/)
  * http://www.goanywheremft.com/solutions/managed-file-transfer
  * [Enhanced File Transfer (EFT)](http://www.globalscape.com/)
  * [Biscom Secure File Transfer](http://www.biscom.com/sft/bds.htm)
  * [JSCAPE MFT Server - Managed File Transfer](http://www.jscape.com/products/file-transfer-servers/jscape-mft-server/)
  * [FTP Poller](http://www.ftppoller.com/)

And there are also few Open Source tools:
  * [SOSFTP](http://www.sos-berlin.com/modules/cjaycontent/index.php?id=271&page=sosftp_introduction_en.htm)
  * [fileXhub CE](http://businessintegrationtechnology.com/CommunityEdition.html)

It already exists a lot of standard protocol (ftp, ftps, sftp, scp, rsync, webdav, etc.) for transferring files from a server A to a server B but each protocol doesn't implements a Managed File Transfer.
The idea of this project is to add a generic MFT procotol Client/Server to the standard file transfer protocol.

Karonte has two components (a Server and a Client) and a simple protocol over HTTP(S).
Karonte Server implements some functionality called "application". Each application could use for creating an MFT client.

This is the typical scenario using Karonte Server:

![http://karonte.googlecode.com/svn/wiki/Karonte_MFT_Diagram.png](http://karonte.googlecode.com/svn/wiki/Karonte_MFT_Diagram.png)

Some features of Karonte Server:
  * Multi-platform (100% pure java)
  * JUnit for TDD
  * Web Server embedded ([Winstone Servlet Container](http://winstone.sourceforge.net))
  * Web Services RESTful
  * Invocation only via POST HTTP or HTTPS
  * Many Output format:
    * XML (javax.xml)
    * JSON ([json-simple](http://code.google.com/p/json-simple))
    * TXT
    * UNIX
  * Some application already developed:
    * status
    * timestamp
    * exists
    * sha1sum
    * md5sum
    * length
    * script
    * exec
    * delete
    * copy
    * move
    * unzip
    * zip
    * canread
    * canwrite
    * tempdir
    * tempfile
    * isfile
    * isdirectory
    * rename
    * oldest
    * newest
    * files
    * version
    * countfiles
    * sendmail

  * Security:
    * HTTPS protocol
    * users (basic authentication)
    * profiles (user enable to call an application)
    * acl (client IP access)
    * grant (directory enabled for reading or writing files)
    * scripts (script executable remotely)
  * Logging [Apache Log4J](http://logging.apache.org/log4j/1.2)
  * Client Java (100% implemented, 106 test cases, 82.7% tested)
  * Client PHP (70% implemented, 30 tests, 189 assertions)
  * Client Ruby (20% implemented)
  * Client Python (20% implemented)
  * Client PERL (20% implemented)
  * Client Linux script (20% implemented)

[![](http://www2.clustrmaps.com/stats/maps-no_clusters/code.google.com-p-karonte--thumb.jpg)](http://www2.clustrmaps.com/user/deb108f4e)