# Manage PGP Keypairs

## Create PGP Key Pair

### Kleopatra

The next step is to generate your keypair so you can encrypt/decrypt messages. Like always, we&#39;ll be going with 4096 bit RSA. You will create a Public and Private key pair with information related to your identity and email address or addresses. This is important to help others locate your public key on the key server.

If we were concerned with anonymity, we would make sure that none of the information used in the key pair could be used to reveal our true identity. The e-mail could be a valid alias for an anonymous email service on the DarkNet or complete gibberish.

Kleopatra should be used to create your key pairs instead of GPA because it will allow you to create a 4096 bit RSA key where GPA will only allow you to create a 2048 bit RSA key.

1. Open up Kleopatra application

[![](RackMultipart20211128-4-dbovmn_html_470fda4a86516a41.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/5i6tnlr1.png)

1. Click &quot;File&quot;, then &quot;New Certificate…&quot;

[![](RackMultipart20211128-4-dbovmn_html_84a24065871090b0.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/u069Ntb1.png)

1. In the Certificate Creation Wizard click &quot;Create a personal OpenPGP key pair&quot;

[![](RackMultipart20211128-4-dbovmn_html_33d945644ed66e55.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/oVaws0J1.png)

1. Enter your personal information, but do not click Next yet.

[![](RackMultipart20211128-4-dbovmn_html_77f12e5df50f08.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/xJFjFGx1.png)

1. Click &quot;Advanced Settings…&quot;, and in the Advanced Settings dialog box in the &quot;Key Material&quot; section select the &quot;RSA&quot; radio button, select &quot;4,096 bits&quot; from the drop-down menu, and click &quot;Ok&quot;

[![](RackMultipart20211128-4-dbovmn_html_85e21a14c187d81d.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/dcOihQG1.png)

1. Verify that the information you entered your information correctly and click &quot;Create Key&quot; [![](RackMultipart20211128-4-dbovmn_html_875023ef0d54dc8c.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/hUIQgMb1.png)
2. Enter a secure passphrase in the &quot;pinentry&quot; dialog box and click &quot;Ok&quot;

[![](RackMultipart20211128-4-dbovmn_html_edbd16b755091cb5.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/kIPFAQF1.png)

1. Kleopatra will now generate the key pair. The random entry of data is used to create entropy. Enter text, move the mouse, etc.

[![](RackMultipart20211128-4-dbovmn_html_c1606ac4ded37daf.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/p8vJdbN1.png)

1. Once the key is created, click &quot;Finish&quot;

[![](RackMultipart20211128-4-dbovmn_html_f50dd61cfb766cef.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/1SRNdt61.png)

### GPA

Next, you want to make a PGP key. Remember, none of the details need to be valid. I&#39;d use your online name or a different alias when making your key. Something that isn&#39;t your gamertag for online games, or anything that may tie to you. A completely new alias. The e-mail doesn&#39;t need to be valid at all. Here are some pictures to help you through the process. Also, make a backup of your key!!!

First, click the keys in the menu at the top. Alternatively, you can click CTRL+N to begin the process of creating a key. Shown here:

![](RackMultipart20211128-4-dbovmn_html_27df0ad15213bcdf.png)

You will go through a set-up, where you make a name for your key, which I suggest you use an alias. Shown here:

![](RackMultipart20211128-4-dbovmn_html_e05f9cff429ed3f9.png)

After selecting your alias, it asks for an e-mail address. This e-mail should be non-existent, and be linked to a website that also doesn&#39;t exist. Shown here:

![](RackMultipart20211128-4-dbovmn_html_e129fd9a28d62d3c.png)

Then you&#39;re asked to make a backup of your key. I highly suggest you do this! Although you can make a back up at any time, you should just do it now. This is where your public key will be that you give to others to contact you. Shown here:

![](RackMultipart20211128-4-dbovmn_html_a0fdcb0c8ee99e56.png)

Find where you put the back up of your key. It will be an .asc file but no worries, when asked to open the file just tell windows or whatever OS to open it using Notepad. Here you will find a public key similar to this.

![](RackMultipart20211128-4-dbovmn_html_a8acd9cda7d1608a.png)

When sharing your key with others, you want to copy and paste from the beginning dashes to the end dashes. Exactly how I have copied and pasted above.

### GPG Suite

\&lt;…\&gt;

## Publish the Public Key to a Key Server

### Kleopatra

Add your public key to a public key server so people can find your public key in order to send you secure messages.

### GPA

Add your public key to a public key server so people can find your public key in order to send you secure messages. A public key can be published to a key server from GPA by clicking on the &quot;Server&quot; menu and selecting &quot;Send Keys.&quot;

### GPG Suite

\&lt;…\&gt;

## Retrieve Public Keys

### Kleopatra

In this step we are going to retrieve the public key from the key pair that was just created. By doing this we are able to make the public key available to those that wish to communicate with you securely. Without it, they will not be able to encrypt messages that you are able to decrypt.

1. In the &quot;My Certificates&quot; tab, right click on your key and click &quot;Export Certificates…&quot;

[![](RackMultipart20211128-4-dbovmn_html_73da137c452d08a8.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/h86y7Le1.png)

1. Browse to the location where you want to save the public key and click &quot;Save&quot; (Note: you may want to give it a name that distinguishes this file as your public key)
2. The public key can be viewed in a text editor, like notepad. Browse to the location where you saved the key and open it. (Note: The key will have a &quot;.asc&quot; extension, you may have to select &quot;All files&quot; from the dropdown menu.

[![](RackMultipart20211128-4-dbovmn_html_be66da901ba71a08.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/XIFqJy81.png)

1. The text you see in the file is your public key. This is the text that you will send to others so they can import it into their PGP application.

[![](RackMultipart20211128-4-dbovmn_html_27599d9bc39eb3c1.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/gJK0c9S1.png)

### GPA

\&lt;…\&gt;

### GPG Suite

\&lt;…\&gt;
