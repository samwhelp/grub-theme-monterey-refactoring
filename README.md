

# Home

| Link | GitHub |
| ---- | ------ |
| [grub-theme-monterey-refactoring](https://samwhelp.github.io/grub-theme-monterey-refactoring/) | [GitHub](https://github.com/samwhelp/grub-theme-monterey-refactoring) |
| [grub-theme-refactoring](https://samwhelp.github.io/grub-theme-refactoring) | [GitHub](https://github.com/samwhelp/grub-theme-refactoring) |
| [grub-theme-refactoring-select](https://samwhelp.github.io/grub-theme-refactoring-select/) | [GitHub](https://github.com/samwhelp/grub-theme-refactoring-select) |




## Subject

* [Theme Source](#theme-source)
* [Theme File](#theme-file)
* [Install](#install)
* [Apply](#apply)
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




## Apply

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

| Region            | Region        | Region             |
| ----------------- | ------------- | ------------------ |
| 1. Northwest (nw) | 2. North (n)  | 3. Northeast (ne)  |
| 4. West (w)       | 5. Center (c) | 6. East (e)        |
| 7. Southwest (sw) | 8. South (s)  | 9. Southeast (se)  |

> menu-box file name

| Region             | Region            | Region             |
| ------------------ | ----------------- | ------------------ |
| 1. menu-box-nw.png | 2. menu-box-n.png | 3. menu-box-ne.png |
| 4. menu-box-w.png  | 5. menu-box-c.png | 6. menu-box-e.png  |
| 7. menu-box-sw.png | 8. menu-box-s.png | 9. menu-box-se.png |




## Branch

| Branch |
| --- |
| [main](https://github.com/samwhelp/grub-theme-monterey-refactoring/tree/main) |
| [gh-pages](https://github.com/samwhelp/grub-theme-monterey-refactoring/tree/gh-pages) |
| [source](https://github.com/samwhelp/grub-theme-monterey-refactoring/tree/source) |
