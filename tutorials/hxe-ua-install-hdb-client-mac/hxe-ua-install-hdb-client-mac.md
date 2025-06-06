---
parser: v2
author_name: John Currie
author_profile: https://github.com/JCurrie27
primary_tag: products>sap-hana\,-express-edition
tags: [ tutorial>beginner, products>sap-hana\,-express-edition ]
time: 10
---

# Installing SAP HANA HDB Client (Mac)
<!-- description --> Install the client package if you intend to develop XS applications on a machine that will not have a local SAP HANA 2.0, express edition installation.

<!-- loio06fe72b1ede54bc88321e15c896eade6 -->

## Prerequisites
 - **Tutorials:** You have completed [Start SAP HANA, express edition Server (VM installations)](http://developers.sap.com/tutorials/hxe-ua-getting-started-vm.html) or [Test the Installation (Native Linux installations)](http://developers.sap.com/tutorials/hxe-ua-test-binary.html)

## You will learn
How to install the SAP HANA client on a Mac, using either a graphical user interface or a command line.

---

## Intro
The `server machine` in these instructions refers to the laptop on which SAP HANA 2.0, express edition is installed, while `client machine` refers to your local machine. You do not need to install the two on the same machine or VM.

The clients let you access SAP HANA 2.0, express edition, from your client machine. This is the Reduced SAP Client package.

The clients included with the SAP HANA HDB client software package are:

-   JDBC

-   ODBC

-   SQLDBC

-   `ODBO/MDX`

-   Python (`PyDBAPI`)

-   `ADO.NET`


### Download the client package


Install the Download Manager to your client machine and download the client package.

1.  Save the Download Manager installation files to your client machine and open it. For instructions on downloading and running the Download Manager, see either the [Installing SAP HANA 2.0, express edition (Binary Installer Method)](http://developers.sap.com/tutorials/hxe-ua-installing-binary.html) or [Installing SAP HANA 2.0, express edition (Virtual Machine Method)](http://developers.sap.com/tutorials/hxe-ua-installing-vm-image.html) tutorials, or go straight to the SAP HANA, express edition [registration page](https://www.sap.com/products/technology-platform/hana/express-trial.html).

2.  In Download Manager, in the `Image` menu, select either `Virtual Machine` or `Binary Installer`.

3.  Click `Browse` and select a directory where your client package will be saved.

4.  Select the `Clients (Mac)` package. Clear the Select boxes of all other packages.

5.  Click `Download`. The `clients_mac.tgz` file downloads to your save directory.

6.  Use a compression utility to extract the compressed clients file.

    This extracts the following files and their contents:

    -   `hdb_client_mac.tgz`

    -   `xs.onpremise.runtime.client_darwinintel64.zip`



### Install the SAP HANA HDB client


To install the SAP HANA client on a Mac machine, do the following:

1.  Go to the directory where you wish to unpack the `hdb_client_mac.tgz` files:

    ```bash
    cd <your_destination>
    ```

2.  Unpack the file:

    ```bash
    sudo tar -xvzf <unzipped_filepath>/hdb_client_mac.tgz
    ```

    The directory `HDB_CLIENT_MACOS` is created.

3.  Navigate to the `HDB_CLIENT_MACOS` directory and run `hdbinst` to start the installer:

    ```bash
    cd HDB_CLIENT_MACOS
    sudo ./hdbinst
    ```

    Follow the instructions on the screen to install the SAP HANA HDB client.



### Log the installation


The system automatically logs the SAP HANA HDB client installation. The log files are stored at `%TEMP%\hdb_client_<time_stamp>` for Windows and `/var/temp/hdb_client_<time_stamp>` for Linux.


### Connect to SAP HANA, express edition


Connect to a SAP HANA 2.0, express edition system using either JDBC or Python:

[Use Clients to Query an SAP HANA Database](https://developers.sap.com/mission.hana-cloud-clients.html)



### Uninstall the SAP HANA HDB client


Each installation has its own uninstallation tool. Use the `hdbuninst` command to uninstall the client software from your command prompt.

```bash
sudo <unzipped_filepath>/HDB_CLIENT_<version>/hdbuninst
```

Follow the instructions on the screen to uninstall the SAP HANA HDB client.

