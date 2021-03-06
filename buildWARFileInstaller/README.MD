# JasperReports Server WAR File Installer

When evaluating JasperReports® Server, the downloads from jaspersoft.com are "bundled installers" that deploy a complete installation with Tomcat and Postgres.

The WAR file installer referred to in the JasperReports Server Installation Guide is more flexible, with repository deployments into Oracle, SQL Server, DB2 and MySQL, and app server installs into Websphere and Weblogic. Also the WAR file installer is needed to do a Docker/Kubernetes deployment - see (https://github.com/TIBCOSoftware/js-docker)

The WAR File Installer for JasperReports Server commercial editions can be downloaded by Jaspersoft customers from edelivery.tibco.com. Or a bundled installer can be used to create a WAR FIle Installer using the process below.

1. Install JasperReports Server using a bundled installer.
1. Stop the installed JasperReports Server.
1. Include the files and directory in this buildWARFileInstaller directory of the js-docker repository into the JasperReports Server install directory you set during the installation.
    * \Jaspersoft\jasperreports-server-VERSION by default on Windows.
1. Open a command line and cd into the JasperReports Server installation directory.
1. Run the scripts
    * (Windows) `.\build-WAR-file-installer`
    * (Linux/Mac) `./build-WAR-file-installer.sh` Probably need to chmod +x the .sh file
1. The WAR file installer file -TIB_js-jrs_VERSION_bin.zip - will be created.
    * There is a working directory - warfile - that can be deleted
1. Running  `./build-WAR-file-installer clean` will remove the WAR file installer file and the warfile directory
