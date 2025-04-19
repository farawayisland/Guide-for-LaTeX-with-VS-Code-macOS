# (La)TeX Installation with Visual Studio Code (macOS)
## Dependencies
- [`Homebrew`](https://brew.sh/)
- [`Visual Studio Code`](https://formulae.brew.sh/cask/visual-studio-code)

You can install the package manager Homebrew along with Visual Studio Code by running the following commands on macOS's `Terminal.app`:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install --cask visual-studio-code
```

## Step 1. Installing a [TeX Distribution](https://tug.org/levels.html)
- [`MacTeX-no-GUI`](https://formulae.brew.sh/cask/mactex-no-gui) (Recommended)
```
brew install --cask mactex-no-gui
```
***or***
- [`TeX Live`](https://formulae.brew.sh/formula/texlive)
```
brew install texlive
```
Afterwards, make sure to update the installed TeX distribution with the following commands:
```
sudo tlmgr update --self
sudo tlmgr update --all
```

Then, create the following three [`texmf`](https://tex.stackexchange.com/a/420623) directories based on the default variables (`TEXMFHOME`, `TEXMFVAR`, `TEXMFCONFIG`)  listed in `/usr/local/texlive/2025/texmf.cnf` (replace `2025` with the specific release year of your TeX distribution):
```
mkdir -p ~/Library/texmf
mkdir -p ~/Library/texlive/2025/texmf-var
mkdir -p ~/Library/texlive/2025/texmf-config
```
For more information, see the following TeX User Group (TUG) documentations: [*A Directory Structure for TeX Files*](https://tug.org/tds/) and [*The TeX Live Guide*, § 2.2 Top level TeX Live directories](https://tug.org/texlive/doc/texlive-en/texlive-en.html#x1-100002.2). You can also read [Francisco Torralbo's *Using the TeX local texmf*](https://www.ugr.es/~ftorralbo/blog/programming/local-texmf/) for a brief summary.

At this point you can also change the default configurations for your (La)TeX compilations such as changing the default paper size:
```
sudo tlmgr paper a4
```

## Step 2. Installing [`LaTeX Workshop`](https://github.com/James-Yu/LaTeX-Workshop)
Go to the [Visual Studio Marketplace web page](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop) and click "Install." You can also install the extension directly from `Visual Studio Code.app` in the `View > Extensions` menu (Command+Shift+X).
