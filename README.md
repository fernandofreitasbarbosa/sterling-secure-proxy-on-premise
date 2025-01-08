# sterling-secure-proxy-on-premise
code to deploy sterling secure proxy on-premise

# Installation of Sterling Secure Proxy Configuration Manager

./SSPcm.V6201.Linux_X64.bin

PRESS <ENTER> TO CONTINUE:

Licenciamento ou digite "1" para aceitar o Contrato/Acordo

Where would you like to install?

  Default Install Folder: /opt/Sterling/SSPcm

ENTER AN ABSOLUTE PATH, OR PRESS <ENTER> TO ACCEPT THE DEFAULT
      :/opt/sspcm

 Enter the SSP Configuration Manager Listen Port #.

ENTER PORT NUMBER, OR PRESS <ENTER> TO ACCEPT DEFAULT (Default: 62366):

PRESS <ENTER> TO CONTINUE:

ENTER THE PASSPHRASE: Password@123
ENTER THE PASSWORD: Password@123

ENTER PORT NUMBER, OR PRESS <ENTER> TO ACCEPT DEFAULT (Default: 8443):

Pre-Installation Summary
------------------------

Please Review the Following Before Continuing:

Product Name:
    IBM Secure Proxy Configuration Manager 6.2.0.1

Install Folder:
    /opt/sspcm

Disk Space Information (for Installation Target):
    Required:     418.971.853 Bytes
    Available: 63.516.835.840 Bytes


===============================================================================
Select Default Key Certificate
------------------------------

Before you can begin production, you must import/generate a secure
certificate. The default configuration uses a single key to secure the
connection between the engine and CM.

    1- Import Key Certificate
    2- Generate Key Certificate

ENTER THE NUMBER OF THE DESIRED CHOICE: 2

===============================================================================
Generate Default Self Signed  Key Certificate
----------------------------------------------

You must provide Alias (Common Name) for the Self Signed Certificate

ENTER Alias, OR PRESS <ENTER> TO ACCEPT DEFAULT (Default: IbmSelfSigned): ssp

===============================================================================
Generate Default Self Signed  Key Certificate
----------------------------------------------

You must provide Store Passphrase for the Self Signed Certificate

Enter the Password: Password@123

===============================================================================
Generate Default Self Signed  Key Certificate
----------------------------------------------

You must provide Export Key Cert Location for the Self Signed Certificate

ENTER Export Key Cert Location, OR PRESS <ENTER> TO ACCEPT DEFAULT (Default:
   /opt/sspcm/defKeyCert.txt):

   ===============================================================================
Generate Default Self Signed  Key Certificate
----------------------------------------------

You must provide Password for KeyCert export

Enter the Password for KeyCert export: Password@123

===============================================================================
Installation Complete
---------------------

Congratulations. IBM Secure Proxy Configuration Manager 6.2.0.1 has been
successfully installed to:

/opt/sspcm

Important Note: With FIPS mode enabled, SSP v6.2.0 does not support
"TLS_RSA_WITH_xxxx" CipherSuites.
To continue using FIPS mode, the SSL Configuration in SSP must be changed to
use a CipherSuite that is still supported.
For more details, refer to the "Known Restrictions" section in SSP v6.2.0
documentation.

# To start the software type
./startCM.sh

# To login
Url to login: https://10.176.40.76:8443/sspcmgui


# Installation of Sterling Secure Proxy Engine

./SSP.V6201.Linux_X64.bin

PRESS <ENTER> TO CONTINUE:

Licenciamento ou digite "1" para aceitar o Contrato/Acordo, 1

===============================================================================
Choose Installation Folder
--------------------------

Where would you like to install?

  Default Install Folder: /opt/Sterling/SSP

ENTER AN ABSOLUTE PATH, OR PRESS <ENTER> TO ACCEPT THE DEFAULT
      :/opt/ssp

INSTALL FOLDER IS: /opt/ssp
   IS THIS CORRECT? (Y/N): y

===============================================================================
Specify Engine Listen Port
--------------------------

Enter the SSP Engine Listen Port #.

ENTER PORT NUMBER, OR PRESS <ENTER> TO ACCEPT DEFAULT (Default: 63366):

===============================================================================
Specify Passphrase
------------------

Enter the passphrase required to unlock the key that allows encryption and
decryption of configuration files.

The passphrase must be 6 to 28 characters string with at least one digit, one
upper case letter, one lower case letter, one special symbol !@#$%^&  and  not
more than 2 consecutive character repetition.

ENTER THE PASSPHRASE:Password@123

===============================================================================
Pre-Installation Summary
------------------------

Please Review the Following Before Continuing:

Product Name:
    IBM Secure Proxy Engine 6.2.0.1

Install Folder:
    /opt/ssp

Disk Space Information (for Installation Target):
    Required:     297.820.247 Bytes
    Available: 63.142.277.120 Bytes

PRESS <ENTER> TO CONTINUE:

===============================================================================
Select Default Key Certificate
------------------------------

Before you can begin production, you must import/generate a secure
certificate. The default configuration uses a single key to secure the
connection between the engine and CM.

    1- Import Key Certificate
    2- Generate Key Certificate

ENTER THE NUMBER OF THE DESIRED CHOICE: 1

===============================================================================
Import Default Key Certificate exported from IBM Configuration Manager
----------------------------------------------------------------------

You must provide file path for the Self Signed Key Certificate

ADD KEYCERT LOCATION : /opt/sspcm/defKeyCert.txt

===============================================================================
Import Default Key Certificate exported from IBM Configuration Manager
----------------------------------------------------------------------

You must provide Password for KeyCert export

Enter Password for KeyCert export :Password@123


===============================================================================
Import Default Key Certificate exported from IBM Configuration Manager
----------------------------------------------------------------------

You must provide Engine Cert Alias for the Self Signed Key Certificate to be
imported

ADD ALIAS (COMMON NAME) : ssp

===============================================================================
Installation Complete
---------------------

Congratulations. IBM Secure Proxy Engine 6.2.0.1 has been successfully
installed to:

/opt/ssp

Important Note: With FIPS mode enabled, SSP v6.2.0 does not support
"TLS_RSA_WITH_xxxx" CipherSuites.
To continue using FIPS mode, the SSL Configuration in SSP must be changed to
use a CipherSuite that is still supported.
For more details, refer to the "Known Restrictions" section in SSP v6.2.0
documentation.

./startEngine.sh

