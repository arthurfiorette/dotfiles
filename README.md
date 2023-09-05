# dotfiles

```bash
# Setup your SSH key
ssh-keygen -t ed25519 -C #<email>
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
echo You key: $(cat ~/.ssh/id_ed25519.pub)

# Setup your GPG key
gpg --full-generate-key
gpg --list-secret-keys --keyid-format=long
gpg --armor --export #<key>

# Runs installer
curl -sSf https://arthur.run/dotfiles/install | sh
```

<br />
