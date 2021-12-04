# Command Line (gpg.exe)

## Create PGP Keypair

Before you can encrypt or sign files with GPG you must have a key.
--- Bash
gpg --gen-key
---
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

