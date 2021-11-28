# Install

## Windows (GPG4Win)

Download: [http://gpg4win.org/download.html](http://gpg4win.org/download.html)

Make sure that Kleopatra and GNU Privacy Assistant (GPA) are installed. GPA is not selected as an option by default. Either Kleopatra or GPA can be used to encrypt and decrypt messages.

1. Choose your language, click &quot;Ok&quot;

[![](RackMultipart20211128-4-dbovmn_html_e53115da50210aaf.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/SUJ3aT21.png)

1. Click &quot;Next&quot;, then &quot;Next&quot; again. You&quot;ll now be at a screen asking what components you want to install. We&#39;ll be selecting &quot;Kleopatra&quot;, &quot;GpgEX&quot;, and &quot;Gpg4win Compendium&quot;. Then click &quot;Next&quot;

[![](RackMultipart20211128-4-dbovmn_html_b2b6267a689e4d14.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/oNLB4Kk1.png)

1. It will ask where to install, just keep the default and click &quot;Next&quot;
2. Now it&#39;ll ask where you want to install shortcuts. Select whichever you want, click &quot;Next&quot;
3. You can choose which Start Menu folder you want it installed in, just click &quot;Next&quot;
4. It will now install, when done you should see this. Click &quot;Next&quot;, then &quot;Finish&quot; [![](RackMultipart20211128-4-dbovmn_html_6e4d881d85af9aa2.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/RYUfaj41.png)

## Linux (GnuPG/Gnu Privacy Assistant)

Like I said in the intro, we&#39;ll be using GnuPG with Gnu Privacy Assistant. I like GPA as a graphical front-end because its layout is really easy to understand and follow.

1. Open up Terminal
2. Type, without quotes, &#39;sudo apt-get install gpa gnupg2&#39;, then hit &#39;enter&#39;
3. Enter your password, hit &#39;enter&#39;
4. It will pull the dependancies needed for both to work properly, tell you the space needed, and ask you to confirm. Type &#39;y&#39; then hit &#39;enter&#39; to confirm
5. Wait a bit as everything installs

This should only take a few minutes to complete. See this picture to confirm you&#39;re doing the steps correctly:

[![](RackMultipart20211128-4-dbovmn_html_64f646618718b6c2.png)](https://www.deepdotweb.com/wp-content/uploads/2015/02/TVjAVPp1.png)

## Mac OS (GPG Suite)

\&lt;…\&gt; [https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-mail](https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-mail)

## iPhone (IPGMail)

\&lt;…\&gt;

# Create PGP Key Pair

## Kleopatra

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

## GPA

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

## GPG Suite

\&lt;…\&gt;

