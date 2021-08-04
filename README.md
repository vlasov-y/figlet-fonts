```
┬─┐o┌─┐┬  ┬─┐┌┐┐  ┬─┐┌─┐┌┐┐┌┐┐┐─┐
├─ ││ ┬│  ├─  │   ├─ │ ││││ │ └─┐
┆  ┆┆─┘┆─┘┴─┘ ┆   ┆  ┘─┘┆└┘ ┆ ──┘
┳━┓o┏━┓┳  ┳━┓┏┓┓  ┳━┓┏━┓┏┓┓┏┓┓┓━┓
┣━ ┃┃ ┳┃  ┣━  ┃   ┣━ ┃ ┃┃┃┃ ┃ ┗━┓
┇  ┇┇━┛┇━┛┻━┛ ┇   ┇  ┛━┛┇┗┛ ┇ ━━┛
```

My collection of ascii art fonts for [figlet](http://www.figlet.org/) or [toilet](http://caca.zoy.org/wiki/toilet). 

Install files to `/usr/share/figlet/` or `/usr/share/figlet/fonts/`.

```shell
curl -Lo- 'https://github.com/vlasov-y/figlet-fonts/archive/refs/tags/v1.1.tar.gz' | sudo tar -C "$(figlet -I2)" --strip-components 1 -xpzvf -
```

```shell
find "$(figlet -I2)" -type f -name '*.*f' | while read -r i; do 
  echo "> $i"
  figlet -f "$i" "$(basename "$i")"
done | less
```
