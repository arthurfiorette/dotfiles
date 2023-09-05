# dotfiles

```bash
# Runs installer
curl -sSf https://arthur.run/dotfiles/install | sh
```

<br />

You may want to setup your keys after the installation:

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

# Setup git config
git config --global user.name #<name>
git config --global user.email #<email>
```