# Public keys for Core Blockchain ecosystem

## Introduction

GPG, or GNU Privacy Guard, is a public key cryptography implementation. This allows for the secure transmission of information between parties and can be used to verify that the origin of a message is genuine.

## How To Import Public Keys

You can import someone’s public key in a variety of ways. If you’ve obtained a public key from someone in a text file, GPG can import it with the following command:

```bash
curl -sSL https://raw.githubusercontent.com/core-coin/keys/master/Name%20(ID).asc | gpg --import -
rm -i "Name (ID).asc"
```

> Please, replace space with `%20` in URL

<dl>
 <dt>Name</dt>
 <dd>Name of the public key</dd>
 <dt>ID</dt>
 <dd>Last 8 characters from fingerprint</dd>
</dl>

## Encrypt and Decrypt Messages with GPG

### Encrypt

You can encrypt messages using the `–encrypt` flag for GPG. The basic syntax would be:

```bash
gpg --encrypt --sign --armor -r name@coreblockchain.cc name-of-file
```

You should include a second “-r” recipient with your own email address if you want to be able to read the encrypted message.

### Decrypt

When you receive a message, simply call GPG on the message file:

```bash
gpg file_name.asc
```
