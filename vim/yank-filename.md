# Vim yank filename

As a basis for adding to `.vimrc`

```vim
" relative path
:let @+ = expand("%")

" full path
:let @+ = expand("%:p")

" just filename
:let @+ = expand("%:t")
```

