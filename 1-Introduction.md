# Summary

The purpose of this post is to explain what PGP is and how to use it to secure communications. While frequently PGP is used together with other tools for anonymity, like Tor or I2P, that is not the purpose of this guide. The PGP encrypted messages do not have to be sent over email. Messages can be easily sent over SMS, Facebook, or any application that will allow you to paste in the encrypted message. The message could also be contained in an encrypted file and sent as an attachment or stored in a shared file system. This guide you will cover the basic tasks required to install a PGP application, create a PGP keypair, encrypt, decrypt, sign, and verify messages, as well as how store, share, and retrieve keys using a public key server.

Applications to enable the use of PGP are available for Windows, Mac, Linux, and mobile devices. This guide will use Kleopatra and GPA as part of the GPG4Win application, or GPG4Win portable, to enable this capability on Windows hosts. The GPG4Win Portable application will allow you to store the application and your keys on a USB device so that it can be used without having to install the application. It can also be run from the local file system for situations when you can&#39;t install applications and are prevented from mounting removable media.

One thing to keep in mind is that PGP cannot protect your messages from situations where the plaintext message may be captured before it is encrypted. For example, a key logger installed on the host used to create the message before it is encrypted will capture the keystrokes used when crafting the message. Also, do not create your messages in a service like Gmail, as the text that you entered could be saved automatically as a &quot;draft&quot; within your account by the service. Instead, craft the message in notepad and only paste the message into Gmail once it is encrypted.

## PGP Background (Wikipedia)

[**https://en.wikipedia.org/wiki/Pretty\_Good\_Privacy**](https://en.wikipedia.org/wiki/Pretty_Good_Privacy)

Pretty Good Privacy is a data encryption and decryption computer program that provides cryptographic privacy and authentication for data communication. PGP is often used for signing, encrypting, and decrypting texts, e-mails, files, directories, and whole disk partitions and to increase the security of e-mail communications.

To the best of publicly available information, there is no known method which will allow a person or group to break PGP encryption by cryptographic or computational means. Indeed, in 1995, [cryptographer](https://en.wikipedia.org/wiki/Cryptographer)[Bruce Schneier](https://en.wikipedia.org/wiki/Bruce_Schneier) characterized an early version as being &quot;the closest you&#39;re likely to get to military-grade encryption.&quot;[[](https://en.wikipedia.org/wiki/Pretty_Good_Privacy#cite_note-2)

# Concepts

PGP allows us to perform one or more of the following tasks; encrypt, decrypt, sign, or verify. This section will describe each of these tasks. It is important to understand how the pubic and private keys are used and by whom for each of these tasks.

\&lt;Keypairs\&gt;

_Encrypt_ takes the recipient&#39;s _public_ key and scrambles a message. This scrambled text is only able to be unscrambled by the recipient&#39;s _private_ key. The _sender_ always _encrypts_ with the _recipient&#39;s public_ key.

_Decrypt_ takes a message that has been _encrypted_ using the recipient&#39;s _public_ key and descrambles it using the recipient&#39;s _private_ key and the passphrase associated with that _private_ key. The recipient always decrypts with the _recipient&#39;s private_ key.

_Sign__ing_ a message authenticates the author the message and provides cryptographic integrity. In other words, it ensures that the message was authored by the owner of the keypair that it was signed with and that it was not tampered with in transit. The _sender_ always signs a message with the _sender&#39;s private_ key and the passphrase associated with it.

_Verify_ing a message is the process of analyzing a signed message, to determine if the signing is true.

Signing and verifying can be thought of as opposites.

Note: Signing a message does not obscure the contents of the message; it only authenticates the sender and verifies that the message hasn&#39;t been altered. However, an encrypted message can also be signed by the author.

Putting it all together

The sender of the message retrieves the recipient&#39;s public key. The public key could be provided to the sender via email, copied off the recipient&#39;s web page by the sender, or some other method. The point is that the public key is &quot;public&quot; so that the sender has access to it.

The sender composes the message and uses the recipient&#39;s public key to encrypt the text.

The sender then copies the encrypted text and pastes it into an email, SMS, Facebook, chat, etc. and sends it. It&#39;s important to note that only the encrypted text is secured. The sender and recipient&#39;s email addresses, subject, and other header information can be read in plain text.

Upon receiving the message, the recipient uses his own private key and password to decrypt the message. This is what makes the private key so important. Only someone with the private key and password, that is from the same key pair as the public key used to perform the encryption, can decrypt the message.

## When should I sign? When should I encrypt?

It is unnecessary to sign and encrypt every outgoing email. Well, then: when should you sign? And when should you encrypt? And when should you do nothing?

You have three rational choices when you are sending a message:

_Do nothing_. If the contents of the email are public (non-confidential), and the recipient does not care whether you or an impostor sent the message, then do nothing. You can send the message as you&#39;ve sent messages your whole life: in plain text.

_Sign, but don&#39;t encrypt_. If the contents of the email are public (non-confidential), but the recipient wants assurance that you -- not an impostor -- actually sent the message, then you should sign but not encrypt. Simply follow the tutorial above, skipping over the encryption and decryption steps.

_Sign and encrypt_. If the contents of the email are confidential, sign and encrypt. It does not matter whether the recipient wants assurance that you sent the message -- _always_ sign when you encrpt.

I do nothing for 90% of emails I send; security is just not necessary. The remaining 10% of the time, I sign and encrypt. Whenever there is confidential information -- business plans, credit card numbers, bank numbers, social security numbers, corporate strategies, etc. -- I sign and encrypt. I define confidential information loosely, because I&#39;d rather sign and encrypt unnecessarily than do nothing and leak sensitive information. As for the third option, I rarely sign, but do not encrypt. Your profession may warrant radically different usage of PGP.

## Why don&#39;t you use PGP MIME attachments? Why don&#39;t you use the Mail.app PGP plugin?

Some PGP nerds prefer sending PGP with attachments (a.k.a., PGP MIME type), instead of using plain text (a.k.a., PGP INLINE).

Conversely, some PGP n00bs want to know why I don&#39;t recommend using a PGP plugin for their email client (i.e., the Mail.app PGP plugin).

Here&#39;s why:

1. Attachments are a pain in the ass.
2. People who use mail plugins for encryption have no idea how they work; the result is a false sense of security.
3. Inline text works places where attachments don&#39;t (the shell, Facebook, iMessage, etc.).
4. The majority of people who have sent me MIME test emails using the Mail.app plugins sent undecryptable messages, because they have no idea what they&#39;re doing or how it works.
5. When a plugin generates an attachment and sends it before you can see what is going on, you have no idea what is happening or if it is working.
6. Lots of applications and email clients do not have PGP built in, so you need inline anyway.

