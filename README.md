# Electronic message security

## Joseph A Streeter

## 2016

# Contents

[Summary 3](#_Toc512342482)

[PGP Background (Wikipedia) 3](#_Toc512342483)

[Concepts 3](#_Toc512342484)

[When should I sign? When should I encrypt? 4](#_Toc512342485)

[Why don&#39;t you use PGP MIME attachments? Why don&#39;t you use the Mail.app PGP plugin? 5](#_Toc512342486)

[Install 6](#_Toc512342487)

[Windows (GPG4Win) 6](#_Toc512342488)

[Linux (GnuPG/Gnu Privacy Assistant) 6](#_Toc512342489)

[Mac OS (GPG Suite) 7](#_Toc512342490)

[iPhone (IPGMail) 7](#_Toc512342491)

[Create PGP Key Pair 8](#_Toc512342492)

[Kleopatra 8](#_Toc512342493)

[GPA 11](#_Toc512342494)

[GPG Suite 13](#_Toc512342495)

[Retrieve Public Keys 14](#_Toc512342496)

[Kleopatra 14](#_Toc512342497)

[GPA 15](#_Toc512342498)

[GPG Suite 15](#_Toc512342499)

[Publish the Public Key to a Key Server 16](#_Toc512342500)

[Kleopatra 16](#_Toc512342501)

[GPA 16](#_Toc512342502)

[GPG Suite 16](#_Toc512342503)

[Obtaining the Private Key 17](#_Toc512342504)

[Kleopatra 17](#_Toc512342505)

[GPA 17](#_Toc512342506)

[GPG Suite 17](#_Toc512342507)

[Importing a Public Key 18](#_Toc512342508)

[Kleopatra 18](#_Toc512342509)

[GPA 18](#_Toc512342510)

[GPG Suite 18](#_Toc512342511)

[Importing the Private Key 19](#_Toc512342512)

[Kleopatra 19](#_Toc512342513)

[GPA 20](#_Toc512342514)

[GPG Suite 21](#_Toc512342515)

[Encrypting a Message 22](#_Toc512342516)

[Kleopatra 22](#_Toc512342517)

[GPA 24](#_Toc512342518)

[GPG Suite 24](#_Toc512342519)

[Decrypting a Message 25](#_Toc512342520)

[Kleopatra 25](#_Toc512342521)

[GPA 26](#_Toc512342522)

[GPG Suite 26](#_Toc512342523)

[Command Line (gpg.exe) 27](#_Toc512342524)

[Create PGP Keypair 27](#_Toc512342525)

[Retrieve the Public Key 27](#_Toc512342526)

[Publish the Public Key 27](#_Toc512342527)

[Obtain the Private Key 27](#_Toc512342528)

[Importing a Private Key 27](#_Toc512342529)

[Encrypting a Message 27](#_Toc512342530)

[Encrypting for Recipient 27](#_Toc512342531)

[Decrypting a Message 27](#_Toc512342532)

[Revoke a key 27](#_Toc512342533)

[Signatures 27](#_Toc512342534)

[Advanced 28](#_Toc512342535)

[Securely Composing Email 28](#_Toc512342536)

[Conclusion 31](#_Toc512342537)

[References 32](#_Toc512342538)


# Retrieve Public Keys

## Kleopatra

In this step we are going to retrieve the public key from the key pair that was just created. By doing this we are able to make the public key available to those that wish to communicate with you securely. Without it, they will not be able to encrypt messages that you are able to decrypt.

1. In the &quot;My Certificates&quot; tab, right click on your key and click &quot;Export Certificates…&quot;

[![](RackMultipart20211128-4-dbovmn_html_73da137c452d08a8.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/h86y7Le1.png)

1. Browse to the location where you want to save the public key and click &quot;Save&quot; (Note: you may want to give it a name that distinguishes this file as your public key)
2. The public key can be viewed in a text editor, like notepad. Browse to the location where you saved the key and open it. (Note: The key will have a &quot;.asc&quot; extension, you may have to select &quot;All files&quot; from the dropdown menu.

[![](RackMultipart20211128-4-dbovmn_html_be66da901ba71a08.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/XIFqJy81.png)

1. The text you see in the file is your public key. This is the text that you will send to others so they can import it into their PGP application.

[![](RackMultipart20211128-4-dbovmn_html_27599d9bc39eb3c1.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/gJK0c9S1.png)

## GPA

\&lt;…\&gt;

## GPG Suite

\&lt;…\&gt;

# Publish the Public Key to a Key Server

## Kleopatra

Add your public key to a public key server so people can find your public key in order to send you secure messages.

## GPA

Add your public key to a public key server so people can find your public key in order to send you secure messages. A public key can be published to a key server from GPA by clicking on the &quot;Server&quot; menu and selecting &quot;Send Keys.&quot;

## GPG Suite

\&lt;…\&gt;

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

# Encrypting a Message

## Kleopatra

To create a message and encrypt it:

1. Open Notepad and create your message
2. Copy the entire message to the clipboard

[![](RackMultipart20211128-4-dbovmn_html_906399d389b29b17.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/fpsVEX21.png)

1. In your task bar, right click on the Kleopatra icon, go to &quot;Clipboard&quot;, then click &quot;Encrypt…&quot; [![](RackMultipart20211128-4-dbovmn_html_12d473ba47d9769c.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/jSeuc6p1.png)
2. This gorgeous window will open. Click &quot;Add Recipient…&quot;

[![](RackMultipart20211128-4-dbovmn_html_46cdc4ff9395341f.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/xmzkSvm1.png)

1. Another window will appear. Click the &quot;Other Certificates&quot; tab, then select who you want to send your message to, then click &quot;Ok&quot;.

[![](RackMultipart20211128-4-dbovmn_html_8c5f94e8ee2e0ba0.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/88SqUA21.png)

1. You should be back at the previous window with the recipient listed. Click &quot;Next&quot; [![](RackMultipart20211128-4-dbovmn_html_83176aec0c07a9bc.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/g4qk0H61.png)
2. If all went well, you should see this window. Click &quot;Ok&quot;

[![](RackMultipart20211128-4-dbovmn_html_4f72118f5011ff6f.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/jnIS7Wo1.png)

1. Your encrypted message will be in your clipboard, all you need to do is paste it into the message box and send

[![](RackMultipart20211128-4-dbovmn_html_caadf7031c2bb940.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/hrQ9tb01.png)

## GPA

![](RackMultipart20211128-4-dbovmn_html_15c12d5557440240.png)

![](RackMultipart20211128-4-dbovmn_html_67cd2bb0e1c7dbc6.png)

![](RackMultipart20211128-4-dbovmn_html_ab27e010265ecdd1.png)

## GPG Suite

\&lt;…\&gt;

# Decrypting a Message

## Kleopatra

![](RackMultipart20211128-4-dbovmn_html_fdec288e68b5b6a8.png)

This is just as easy as encrypting.

1. Copy everything that was sent

[![](RackMultipart20211128-4-dbovmn_html_b18edfb177d62674.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/aj50dmL1.png)

1. In your task bar, right click on the Kleopatra icon, go to &quot;Clipboard&quot;, then click &quot;Decrypt/Verify…&quot;

[![](RackMultipart20211128-4-dbovmn_html_b6e99681ca359a77.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/T8lqyCo1.png)

1. A window will pop up asking for your passphrase, enter that then click &quot;Ok&quot;

[![](RackMultipart20211128-4-dbovmn_html_5acba56382f77f25.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/yj6ciCG1.png)

1. A window should pop up verifying it was decrypted, and copied to your clipboard. Click &quot;Finish&quot;
2. Open your text editor of choice, and paste your message

[![](RackMultipart20211128-4-dbovmn_html_e7a9cb94a1246631.png)](http://www.deepdotweb.com/wp-content/uploads/2015/02/ENJY7tp1.png)

## GPA

\&lt;…\&gt;

## GPG Suite

\&lt;…\&gt;

# Command Line (gpg.exe)

## Create PGP Keypair

Before you can encrypt or sign files with GPG you must have a key.

gpg --gen-key

## Retrieve the Public Key

Post the public, ascii side of your key to the web

gpg --import key.asc

gpg --list-keys

## Publish the Public Key

gpg --armor --output public.asc --export &#39;Your Name&#39;

gpg --send-keys &#39;Your Name&#39; --keyserver hkp://subkeys.pgp.net

gpg --search-keys &#39;myfriend@his.isp.com&#39; --keyserver hkp://subkeys.pgp.net

## Obtain the Private Key

gpg --armor --export-secret-key --output private.asc --export &#39;Your Name&#39;

## Importing a Private Key

gpg

## Encrypting a Message

Here we encrypt/decrypt a file that is just for our own use.

gpg --encrypt --recipient &#39;Your Name&#39; foo.txt

## Encrypting for Recipient

gpg --encrypt --recipient &#39;myfriend@his.isp.net&#39; foo.txt

## [Decrypting a Message](#_Toc469514821)

gpg --output foo.txt --decrypt foo.txt.gpg

## Revoke a key

gpg --gen-revoke --output revoke.txt --export &#39;Your Name&#39;

## Signatures

gpg --verify crucial.tar.gz.asc crucial.tar.gz

gpg --armor --detach-sign your-file.zip

# Advanced

## Securely Composing Email

#### Metadata

Metadata provides the context to the content of the email. Protecting the email content (with PGP) will significantly enhance the security of the communication. Frequently, the context (the metadata) is sufficient to learn a great deal about the communication even without the content. Unfortunately, even PGP encrypted email leaves communications metadata exposed, this includes:

- Subject
- To
- From
- Dates and times
- IP addresses
- email application

Minimizing the contextual information leakage from the email starts with knowing what metadata will be exposed. Where possible, and relevant, take control over that information and unlink it from data linked to you. For example, you can control the From field by creating a new email account. The IP address of the sending email client can be changed by using a VPN, Tor, or a public Internet connection. One option to consider is the use of Tor. The usual caveats about Tor apply: do not rely exclusively on Tor, if you need to protect your IP address then use an IP address that is not attributable to you.

#### The Subject

There is little else you can do about the To, From, and IP, as those are controlled by the infrastructure. However, you have complete control over the Subject. All acceptable subjects are listed below:

- ...
- xxx
- ;;;
- :::
- \&lt;space\&gt;

The Subject must never ever refer to the content of the email, even obliquely. For example, &quot;Subject: Your cocaine has shipped!&quot; is a total email security failure.

- **Subjects should be empty**!
  - Disable the _Warn about empty subject_ setting on your email client

#### Writing

There are fundamentally two options when composing an email: you can either write the email in a text editor, or in an email client. For security, that is, control over the process, a text editor is safer. For convenience most people will use their email client.

- Safest
  - Write in a text editor
  - Encrypt on the command line
  - Only expose already-encrypted data to the email client
- Realistic
  - At least restrict the plaintext to the local system you control

#### Drafts

- Don&#39;t save Drafts in plaintext

Drafts can be a significant source of risk. The storage and handling of drafts must be approached with care. Make sure that they are encrypted (never stored in plaintext), that they are stored locally (where you can be sure of deleting them) and that they are deleted after use. Make sure to configure your email client to store drafts locally and to encrypt them before writing them to disk.

- Don&#39;t store on server
- Ensure they are encrypted
- Ensure they are deleted after use

#### Composition

- Delete the content in a reply, only quote the relevant parts if necessary

Mitigate against the potential threat of any single email being compromised by limiting the information within any single email. The more information is stored in the mental context of the correspondents, the less useful the information in the email is to an adversary. Wherever possible minimize the amount of irrelevant contextual information within the email body. Keep it short, simple, and clean.

#### Attachments

- PGP has all the capability of tar or zip.

It is possible to include all the files you need to include as a pure PGP messages without having an attachment called secret-leaked-nsa-docs.tar.gz.gpg.asc. The program to use is gpg-zip and it takes both --tar= command line options and gpgcommand line options. Use this to bundle your files and send them as an opaque encrypted blob.

#### Encrypting

- use --throw-keys to prevent leaking more metadata

PGP encryption stores metadata about the decryption keys in the encrypted data. This is a simple optimization to allow the recipient to rapidly determine whether the email can be decrypted by a private key they possess. This information also allows an attacker to determine who can read the email. If the email is intended to be truly anonymous, this metadata must be discarded. Fortunately, there is a gpg command line flag for this: --throw-keys.

Ensure that --throw-keys is added to the command line when encrypting data.

- PGP/MIME and inline PGP -ear aren&#39;t the same.

For more control and compatibility, use inline PGP.

#### Sending

Ensure you encrypt by default

Accidentally sending an unencrypted email is a potentially fatal error. Configure your email client to always encrypt by default. If you want to send a plaintext email, then deliberately set that option.

Think about signing

Signing an email provides guarantees that the content was written by someone that possess the private key. That it is, it positively identifies at least one person involved in the email exchange. Think carefully about whether you want to be positively identified as the author of the email. Set your email client to not sign messages by default.

Sign messages explicitly.

Store sent messages locally, then delete them

After the email has been sent and is no longer operationally useful, delete it. To make sure that you can do this, configure your email client to store your _Sent_ messages locally. When in doubt, store locally. At least you will have some control over whether it is thoroughly deleted.

#### Receiving

- Delete emails after they are no longer necessary
- INBOX ZERO
- OUTBOX ZERO
- DRAFTS ZERO
- TRASH ZERO
- Regularly delete all emails. Easiest way is to set the Trash to erase everything after 30 days, and then delete every email after it has been processed.

#### Riseup.net PGP Configuration Guide

There is a PGP configuration guide from riseup.net. If you want to incorporate their best practice recommendations without any of their terrible advice about using key servers etc, then simply install this gpg.conf into your ~/.gnupg.

- [gpg.conf](https://github.com/stribika/duraconf/blob/master/configs/gnupg/gpg.conf)

#### Outreach

- Remind your correspondents to practice the same PGP hygiene

# Conclusion

This should provide you with enough information to get started with PGP/GPG on a Windows host. While PGP can seem complicated at first it&quot;s actually pretty simple. With this technology you can secure nearly all of your electronic communications.

Terms

- PGP – Pretty Good Privacy
- GPG4Win – An OpenGPG compliant application for Windows
- GPG4Win Portable – A GPG4Win application designed to be run from a thumb drive
- Key pair – Public and Private keys generated by a PGP user
- Public key – Key used to encrypt a message to be sent
- Private key – Key used to decrypt a message that has been received
- Key server – A publicly available repository of public PGP keys
- Tor – Client used to provide anonymity and access to the DeepWeb
- I2P – Client used to provide anonymity and access to the DeepWeb
- iPGMail – A PGP client for the iPhone
- Tails – A Linux distribution that combines Tor, PGP, Pidgin OTR, and others for anonymous communications
- Pidgin Off The Record (OTR) – An add-on to the Pidgin chat application that provides PGP encrypted chat capability

# References

- https://www.deepdotweb.com/2015/02/21/pgp-tutorial-for-windows-kleopatra-gpg4win/
- https://www.deepdotweb.com/2013/11/11/pgp-tutorial-for-newbs-gpg4win/
- https://en.wikipedia.org/wiki/Pretty\_Good\_Privacy
- http://notes.jerzygangi.com/the-best-pgp-tutorial-for-mac-os-x-ever/
- http://www.techrepublic.com/blog/it-security/using-gnupg-encryption-tools-with-gpg4win/
- https://gpgtools.tenderapp.com/kb/how-to/first-steps-where-do-i-start-where-do-i-begin-setup-gpgtools-create-a-new-key-your-first-encrypted-mail
- https://github.com/nask0/Operational-PGP
- http://edoceo.com/cli/gpg
- https://riseup.net/en/security/message-security/openpgp/best-practices
- https://riseup.net/en/security/message-security/openpgp/gpg-keys
- https://blog.dest-unreach.be/2009/04/13/the-internals-of-a-gpgpgp-key
- https://futureboy.us/pgp.html
