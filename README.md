# flareon-apps

Application stacks deployed on Flareon node.

Contains the following services:

- BKSP ID (Logto)
- B4CKSP4CE Wiki (Outline)
- BKSP Passwd (Vaultwarden)
- Swynca (our own accounting system)

## Teleport

Note that except of these services, there is also a Teleport instance running on the node.
It is used for SSH access to the node and for accessing sensitive services – BKSP ID Admin and Passwd.

## Encryption

Sensitive configuration data is stored in .env files and encrypted using `envienc` package.
To decrypt or re-encrypt the data, use the following commands:

```sh
# Install envienc in this repo
# If you've already installed it globally, you can skip this step.
npm ci

# Decrypt
npx envienc decrypt

# Encrypt again (if you've made changes to the .env files)
npx envienc encrypt

```
