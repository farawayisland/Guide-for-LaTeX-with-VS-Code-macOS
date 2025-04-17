# (La)TeX Installation with Visual Studio Code (macOS)
## Dependencies
- [`Homebrew`](https://brew.sh/)
- [`Visual Studio Code`](https://formulae.brew.sh/cask/visual-studio-code)

You can install the package manager Homebrew along with Visual Studio Code by running the following commands on macOS's `Terminal.app`:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
```
brew install --cask visual-studio-code
```

## Installing a [TeX Distribution](https://tug.org/levels.html)
### [`MacTeX-no-GUI`](https://formulae.brew.sh/cask/mactex-no-gui) (Recommended)
```
brew install --cask mactex-no-gui
```
### [`TeX Live`](https://formulae.brew.sh/formula/texlive)
```
brew install texlive
```
## Installing [`LaTeX Workshop`](https://github.com/James-Yu/LaTeX-Workshop)
Go to the [Visual Studio Marketplace web page](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) and click "Install." You can also install the extension directly from `Visual Studio Code.app` in the `View > Extensions` menu (Command+Shift+X).
