# Electronic message security

Joseph A Streeter
2016

# Summary

The purpose of this post is to explain what PGP is and how to use it to secure communications. While frequently PGP is used together with other tools for anonymity, like Tor or I2P, that is not the purpose of this guide. The PGP encrypted messages do not have to be sent over email. Messages can be easily sent over SMS, Facebook, or any application that will allow you to paste in the encrypted message. The message could also be contained in an encrypted file and sent as an attachment or stored in a shared file system. This guide you will cover the basic tasks required to install a PGP application, create a PGP keypair, encrypt, decrypt, sign, and verify messages, as well as how store, share, and retrieve keys using a public key server.

Applications to enable the use of PGP are available for Windows, Mac, Linux, and mobile devices. This guide will use Kleopatra and GPA as part of the GPG4Win application, or GPG4Win portable, to enable this capability on Windows hosts. The GPG4Win Portable application will allow you to store the application and your keys on a USB device so that it can be used without having to install the application. It can also be run from the local file system for situations when you can&#39;t install applications and are prevented from mounting removable media.

One thing to keep in mind is that PGP cannot protect your messages from situations where the plaintext message may be captured before it is encrypted. For example, a key logger installed on the host used to create the message before it is encrypted will capture the keystrokes used when crafting the message. Also, do not create your messages in a service like Gmail, as the text that you entered could be saved automatically as a &quot;draft&quot; within your account by the service. Instead, craft the message in notepad and only paste the message into Gmail once it is encrypted.

## PGP Background (Wikipedia)

[**https://en.wikipedia.org/wiki/Pretty\_Good\_Privacy**](https://en.wikipedia.org/wiki/Pretty_Good_Privacy)

Pretty Good Privacy is a data encryption and decryption computer program that provides cryptographic privacy and authentication for data communication. PGP is often used for signing, encrypting, and decrypting texts, e-mails, files, directories, and whole disk partitions and to increase the security of e-mail communications.

To the best of publicly available information, there is no known method which will allow a person or group to break PGP encryption by cryptographic or computational means. Indeed, in 1995, [cryptographer](https://en.wikipedia.org/wiki/Cryptographer)[Bruce Schneier](https://en.wikipedia.org/wiki/Bruce_Schneier) characterized an early version as being &quot;the closest you&#39;re likely to get to military-grade encryption.&quot;[[](https://en.wikipedia.org/wiki/Pretty_Good_Privacy#cite_note-2)

### Contents

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
