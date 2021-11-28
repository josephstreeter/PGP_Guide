# Obtaining the Private Key

## Kleopatra

Similar to obtaining your public key

1. Right click on your key in the &quot;My Certificates tab and select &quot;Export Secret Keys…&quot;

[![](RackMultipart20211128-4-dbovmn_html_5a5698bc21842c67.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/KBWbUBC1.png)

1. Select the location to save your private key, give it a name, check &quot;ASCII armor&quot;, and click &quot;Ok&quot; [![](RackMultipart20211128-4-dbovmn_html_314b128b4d0af021.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/d4MPQKB1.png)

The following dialog box confirms the export of your private key. (Remember to keep the private key safe and never share it!)

1.

[![](RackMultipart20211128-4-dbovmn_html_d4445f32cef25c9d.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/M4osyVS1.png)

## GPA

\&lt;…\&gt;

## GPG Suite

\&lt;…\&gt;

# Importing a Public Key

## Kleopatra

It&#39;s impossible to send a vendor an encrypted message without their public key. The public key could be sent to you in an email as an attachment or included in the signature block, downloaded from a key server, shared from removable storage, etc.

1. Receive a public key as a text file through email or other electronic method
2. Copy all text including &quot;—–BEGIN PGP PUBLIC KEY BLOCK—–&quot; and &quot;—–END PGP PUBLIC KEY BLOCK—&quot;

[![](RackMultipart20211128-4-dbovmn_html_63bbdaafa36dd25d.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/69UnFPR1.png)

1. In your task bar, right click on the Kleopatra icon, go to &quot;Clipboard&quot;, then click &quot;Certificate Import&quot;

[![](RackMultipart20211128-4-dbovmn_html_b0c22af227ae7ea4.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/UG15ss61.png)

1. If the import worked you should see a window pop up as confirmation, click &quot;Ok&quot;

[![](RackMultipart20211128-4-dbovmn_html_e90c001dbff5beb4.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/J9kQIQB1.png)

1. The imported key should now be displayed in Kleopatra under the &quot;Other Certificates&quot; tab [![](RackMultipart20211128-4-dbovmn_html_f612945335560c0c.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/2G438Pi1.png)

## GPA

\&lt;…\&gt;

## GPG Suite

\&lt;…\&gt;

# Importing the Private Key

## Kleopatra

The private key that you will be importing is from a key pair that you have previously created. This private key is used to sign outgoing messages and to decrypt incoming messages. Any host or device that contains your private key should be considered &quot;sensitive&quot; because loss or theft could lead to the compromise of your private key.

1. Click &quot;File&quot;, &quot;Import Certificates…&quot;

[![](RackMultipart20211128-4-dbovmn_html_a3218b35dea88f5e.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/hHDqxpO1.png)

1. Browse to the location where the private key is saved, select it, and click &quot;Open&quot; [![](RackMultipart20211128-4-dbovmn_html_29193379727ffc89.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/Qq8OmEn1.png)
2. A window will be displayed confirming the import of the private key. Click &quot;Ok&quot; to contintue.[![](RackMultipart20211128-4-dbovmn_html_3746bf5bf345edac.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/m6YsDUv1.png)
3. The key information should now be displayed in the &quot;My Certificates&quot; tab[![](RackMultipart20211128-4-dbovmn_html_b7b0eb7e933539f9.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/SyPzPmp1.png)

## GPA

You see people giving their public keys away so others can contact them. Simply open a notepad file, copy and paste their key and import it using the GPA program. I will show you how to do this.

First make a blank text file and copy the users pubic key to it. Shown here:

![](RackMultipart20211128-4-dbovmn_html_a8acd9cda7d1608a.png)

Then, in the Keys menu where you made your key, select import keys. Shown here:

![](RackMultipart20211128-4-dbovmn_html_840f2828ec1de405.png)

![](RackMultipart20211128-4-dbovmn_html_d6e2e6ad737bb6ec.png)

## GPG Suite

\&lt;…\&gt;
