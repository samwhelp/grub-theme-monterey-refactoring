

# Home


| Link | GitHub |
| ---- | ------ |
| [grub-theme-monterey-refactoring](https://samwhelp.github.io/grub-theme-monterey-refactoring/) | [GitHub](https://github.com/samwhelp/grub-theme-monterey-refactoring) |




## Subject

* [Theme Source](#theme-source)
* [Theme File](#theme-file)
* [Install](#install)
* [Config](#config)
* [Docs](#docs)




## Theme Source

| Theme Source |
| ------ |
| [Pling](https://www.pling.com/p/1577873/) |
| [GitHub](https://github.com/sandesh236/monterey-grub-theme) |





## Theme File

| Theme File                       |
| -------------------------------- |
| [theme.txt](https://github.com/samwhelp/grub-theme-monterey-refactoring/blob/main/theme.txt)           |
| [background.jpg](https://github.com/samwhelp/grub-theme-monterey-refactoring/blob/main/background.jpg) |




## Install

run

``` sh

mkdir -p "./tmp"

wget -c "https://github.com/samwhelp/grub-theme-monterey-refactoring/archive/refs/heads/main.tar.gz" -O "./tmp/grub-theme-monterey-refactoring-main.tar.gz"


tar xf "./tmp/grub-theme-monterey-refactoring-main.tar.gz" -C "./tmp"


sudo mkdir -p "/boot/grub/themes"

sudo cp -rf "./tmp/grub-theme-monterey-refactoring-main/." "/boot/grub/themes/grub-theme-monterey-refactoring"

```

or run remote script [fetch.sh](https://github.com/samwhelp/grub-theme-monterey-refactoring/blob/main/helper/theme-installer/fetch.sh)

``` sh
bash <(curl -L 'https://raw.githubusercontent.com/samwhelp/grub-theme-monterey-refactoring/main/helper/theme-installer/fetch.sh')
```




## Config

edit `/etc/default/grub`

```
GRUB_BACKGROUND='/boot/grub/themes/grub-theme-monterey-refactoring/background.jpg'
GRUB_THEME="/boot/grub/themes/grub-theme-monterey-refactoring/theme.txt"
```

or create file `/etc/default/grub.d/theme.cfg`, run

``` sh
cat << EOF | sudo tee /etc/default/grub.d/theme.cfg
GRUB_BACKGROUND='/boot/grub/themes/grub-theme-monterey-refactoring/background.jpg'
GRUB_THEME="/boot/grub/themes/grub-theme-monterey-refactoring/theme.txt"

EOF
```


then run

``` sh
sudo update-grub
```

or run

``` sh
sudo grub-mkconfig -o /boot/grub/grub.cfg
```




## Docs

| Grub Docs |
| ---- |
| [Theme file format](https://www.gnu.org/software/grub/manual/grub/html_node/Theme-file-format.html) |




## Styled Boxes

| Block          | Block      | Block          |
| ---------------| ---------- | -------------- |
| Northwest (nw) | North (n)  | Northeast (ne) |
| West (w)       | Center (c) | East (e)       |
| Southwest (sw) | South (s)  | Southeast (se) |




## Branch

| Branch |
| --- |
| [main](https://github.com/samwhelp/grub-theme-monterey-refactoring/tree/main) |
| [gh-pages](https://github.com/samwhelp/grub-theme-monterey-refactoring/tree/gh-pages) |
| [source](https://github.com/samwhelp/grub-theme-monterey-refactoring/tree/source) |
