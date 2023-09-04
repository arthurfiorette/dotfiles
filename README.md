# dotfiles

```bash
# Setup your SSH key
ssh-keygen -t ed25519 -C #<email>
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
echo You key: `$(cat ~/.ssh/id_ed25519.pub)`

# Setup your GPG key
gpg --full-generate-key
gpg --list-secret-keys --keyid-format=long | awk -F: '/^pub:/ { print $5 }'
gpg --armor --export #<key>

# Runs installer
sh -c "$(curl -fsSL https://arthur.run/dotfiles/install)"
```

<br />
