# Linux Aliases

```bash
################
#    PACMAN    #
################
alias -g paccc='yes | sudo pacman -Scc'
alias -g pacof='sudo pacman -Rncs $(pacman -Qtdq) 2> /dev/null'
alias -g pacqs='pacman -Qs'
alias -g pacrm='sudo pacman -Rncs'
alias -g pacug='sudo pacman -Syyuu'
alias -g pacup='sudo pacman -Syu'
alias -g pacqq='pacman -Qq'
alias -g pacqi='pacman -Qi'
alias -g pacss='pacman -Ss'
alias -g pacsi='pacman -Si'
alias -g pacin='sudo pacman -S'
##############
#    PARU    #
##############
alias -g paru='paru --skipreview --cleanafter'
alias -g parin='paru -S'
alias -g parup='paru -Syu'
alias -g parug='paru -Syyuu'
alias -g parrm='paru -Rncs'
alias -g parcc='yes | paru -Scc'
alias -g parqq='paru -Qq'
alias -g parqi='paru -Qi'
alias -g parss='paru -Ss'
alias -g parsi='paru -Si'
alias -g parof='paru -Rncs $(paru -Qtdq) 2> /dev/null'
alias -g porphans='pacof && parof'

################
#    SYSTEM    #
################
alias -g chmodx='chmod u+x'
alias -g c=clear
alias -g rmrf='rm -rf'
alias -g du='du -hcs'
alias -g ll='exa -abghHlS --icons --octal-permissions'
alias -g lld='exa -abdghHlS --icons --octal-permissions'
alias -g svim='sudo vim'
alias -g snvim='sudo nvim'
alias -g dush='du -sh'
alias -g dfh='df -Th'
alias -g lsblk='lsblk -f'
alias -g v=vim
alias -g m=micro
alias -g sv='sudo vim'
alias -g sm='sudo micro'
alias -g mv='mv -ni'
alias -g fempty='find $(pwd) -empty -type f -delete'
alias -g dempty='find $(pwd) -empty -type d -delete'

################
#    python    #
################
alias -g ipy="python -c 'import IPython; IPython.terminal.ipapp.launch_new_instance()'"

################
#      tar     #
################
alias -g targz='tar xzvf'
alias -g tarbz='tar xjvf'
alias -g tarxz='tar xJvf'

################
#      git     #
################
alias -g gitlink="git config --get remote.origin.url"

################
#      TeX     #
################
alias -g tlmgr="${TEXMFDIST}/scripts/texlive/tlmgr.pl --usermode"

################
#    System    #
################
alias -g aria2c='aria2c -x10'
alias -g ciommu='sudo dmesg | grep -e DMAR -e IOMMU'

#############
# systemctl #
#############
alias -g sctl='sudo systemctl'
alias -g scstart='sctl start'
alias -g scstop='sctl stop'
alias -g screstart='sctl restart'
alias -g scenable='sctl enable'
alias -g scdisable='sctl disable'
alias -g scstatus='sctl status'
alias -g bctl=bluetoothctl
alias -g jctl=journalctl
alias -g mounted='sctl -t mount'

########
# MISC #
########
alias -g ping='ping -c4'
alias -g update-clam='sctl start clamav-daemon && sudo freshclam --show-progress && sctl stop clamav-daemon'
alias -g pipupgrade="pip install --upgrade $(pip list | gawk 'NR>2 {print $1}' | sed -z 's/\n/ /g;s/ $/\n/')"
alias -g lvup="lvim +LvimUpdate +q"
alias -g lv=lvim
alias -g winkey='sudo strings /sys/firmware/acpi/tables/MSDM'
alias -g df='df -h'
alias -g tobios='sudo systemctl reboot --firmware-setup'
alias -g open=xdg-open

##############
# frameworks #
##############
alias solidjs='npx degit solidjs/templates/ts'
```
