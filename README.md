# Configurations


## 1) steps to configure iTerm with ohMyZsh and PowerLevel10k

````
# Configure Powerlevel10k with Zsh

# 1 First install iTerm

# 2 installing ohMyZsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

# 3 installing Powerlevel10k
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >> ~/.zshrc


# 4 changing theme 
# sed -i '' 's/ZSH_THEME=.*/ZSH_THEME="powerlevel10k"/' ~/.zshrc
source ~/.zshrc

# 5 quit and restart iTerm
exec zsh

# 6 for full experience install plugins such as syntaxhighlight and prompt suggestions

````

#### Change iterm for natural text editing 

- Go to Preferences... > Profiles > Keys (not Preferences... > Keys)
- On current versions (3.14+) you then switch to the Key Mappings tab
- Press Presets... dropdown button.
- Select Natural Text Editing

*source: https://apple.stackexchange.com/a/293988*


## 2 Adding to `.gitconfig`

```
shortcut 
[i18n]
    filesEncoding = utf-8
[merge]
    tool = meld
[alias]
    st = status
    ci = commit
    br = branch
    co = checkout
    fa = fetch --all
    df = diff
    dc = diff --cached
    lg = log -p
    lol = log --graph --decorate --pretty=oneline --abbrev-commit
    lola = log --graph --decorate --pretty=oneline --abbrev-commit --all
    ls = ls-files
    ign = ls-files -o -i --exclude-standard
    last = reflog -1
    lasts = reflog -10
    st = status
    br = branch
    cm = commit --reset-author -c HEAD
    amenda = commit -a --amend --no-edit
    amend = commit --amend --no-edit
    du = diff @{upstream}
    dud = diff dev @{upstream}
    dum = diff master @{upstream}
    last = log -1 HEAD --stat
    loli = "!f() { git log $1 --pretty=format:\"%C(yellow)%h%Cred%d\\\\ %Creset%s%Cgreen\\\\ [%ae,%ar]\" --decorate --graph; }; f"
[color]
    ui = auto
[color "branch"]
    current = yellow reverse
    local = yellow
    remote = green
[color "diff"]
    meta = yellow bold
    frag = magenta bold
    old = red bold
    new = green bold
[color "status"]
    added = yellow
    changed = green
    untracked = cyan
[core]
    editor = nano
    autocrlf = false
[branch]
    autosetupmerge = false
[fetch]
    prune = true
    prune-tags = true
[filter "lfs"]
    clean = git-lfs clean -- %f
    smudge = git-lfs smudge -- %f
    required = true
    process = git-lfs filter-process
[pull]
    rebase = true
[core]
    editor = nano
```


# Brew
If you install brew you can deactivate anlaytics send to google with the following commands:
`brew analytics off`

*source: https://docs.brew.sh/Analytics*
