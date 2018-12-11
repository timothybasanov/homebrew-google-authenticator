This is not an official Google product.

# This project is deprecated and should not be used
Use `brew install google-authenticator-libpam` instead and follow the instructions.

# Homebrew formula for Google Authenticator

Enables Google Authenticator as a two-factor authentication
for Mac OS X ssh.

```shell
brew tap timothybasanov/google-authenticator
brew install google-authenticator
echo "auth required /usr/local/lib/security/pam_google_authenticator.so nullok" \
     | sudo tee -a /etc/pam.d/sshd
google-authenticator --force --time-based --disallow-reuse --rate-limit=3 \
     --rate-time=30 --window-size=10
```

See https://github.com/google/google-authenticator-libpam
for more information.
