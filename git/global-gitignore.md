# Global Git Ignore

For files that shouldn't be committed to any project, I use a global `.gitignore` (notes.txt, .tern-port, etc.)

```git
// create and edit ~/.gitignore
git config --global core.excludesfile ~/.gitignore
```

