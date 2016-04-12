`/etc/ansible/roles/common/files/`
==================================

<!---
The tasks here should be:

1. Copy `vimrc` to `~/.vimrc`
2. Copy `vimrc-real` to `~/.config/vim/vimrc`
3. Copy the directory `vim` to `~/.vim`
4. Copy the directory `git` to `~/.config/git`
-->

Treat this directory as a virtual '/' for the common role and copy all files 
to their appropriate places in the hierarchy
