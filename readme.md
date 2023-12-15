## Extracting themes from Rouge

### Install Rouge:
```zsh
gem install rouge
```

### To extract all themes:

```zsh

themes=("base16" "base16.dark" "base16.light" "base16.monokai" "base16.monokai.dark" "base16.monokai.light" "base16.solarized" "base16.solarized.dark" "base16.solarized.light" "bw" "colorful" "github" "gruvbox" "gruvbox.dark" "gruvbox.light" "igorpro" "magritte" "molokai" "monokai" "monokai.sublime" "pastie" "thankful_eyes" "tulip")

for theme in "${themes[@]}"; do
    rougify style "${theme}" > "${theme}.css"
done
```

### To extract a single theme:

```zsh
rougify style base16 > base16.css
```