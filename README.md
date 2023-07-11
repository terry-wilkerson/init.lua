### ThePrimeagen's init.lua
Prerequisite: install [ripgrep](https://github.com/BurntSushi/ripgrep).

[The full video of me setting up this repo](https://www.youtube.com/watch?v=w7i4amO_zaE)

For anyone that is interested in my vimrc, i will have a commit log below
documenting each one of my commits (easy to C-f the change you want to know
about though i would just suggest `git log -S`).

### Windows Setup

1. Install [ripgrep](https://github.com/BurntSushi/ripgrep)
2. Install [https://www.msys2.org/](https://www.msys2.org/)
3. Run `pacman -S mingw-w64-ucrt-x86_64-gcc` in the UCRT64 terminal that was installed
4. Run `pacman -S --needed base-devel mingw-w64-x86_64-toolchain` in the UCRT64 terminal
5. Add an environment path to `C:\msys64\mingw64\bin` or where ever you installed at
6. Check that you can access via Windows Terminal by running
    ``` shell
    gcc --version
    g++ --version
    gdb --version
    ```
7. Clone the init.lua repo into %localappdata%/nvim
8. Install NVim with 
   ``` shell
   winget install Neovim.Neovim
   ```
9.  Install NVim Packer with 
    ``` ps
    git clone https://github.com/wbthomason/packer.nvim "$env:LOCALAPPDATA\nvim-data\site\pack\packer\start\packer.nvim"
    ```
10. Open NVim with 
    ``` ps
    nvim $Env:localappdata/nvim
    ```
11. NVim should go through the setup process. Just to make sure everything is updated, navigate to `./lua/theprimeagen/pakcer.lua` and issue the Vim cmd `:PackerSync`
12. Also verify the treesitter parsers are installed with Vim command: `:checkhealth nvim-treesitter`

**Refer to [https://code.visualstudio.com/docs/cpp/config-mingw](https://code.visualstudio.com/docs/cpp/config-mingw) for instructions if needed

### Change Log
* [33eee9ad](https://github.com/ThePrimeagen/init.lua/commit/33eee9ad0c035a92137d99dae06a2396be4c892e) initial commits
* [cb210006](https://github.com/ThePrimeagen/init.lua/commit/cb210006356b4b613b71c345cb2b02eefa961fc0) netrw, autogroups for yank highlighting, and auto remove whitespace
* [c8c0bf4a](https://github.com/ThePrimeagen/init.lua/commit/c8c0bf4aeacd0bd77136d9c5ee490680515a106b) zenmode.  i really like this plugin
* [81c770d2](https://github.com/ThePrimeagen/init.lua/commit/81c770d2d2e32e59916b39c7f5babbc8560f7a82) copilot testing
* [4a96e645](https://github.com/ThePrimeagen/init.lua/commit/4a96e6457b0a0241ca7361ce62177aa6b9a33a38) fugitive mappings for push and pull
* [a3bad06a](https://github.com/ThePrimeagen/init.lua/commit/a3bad06a4681c322538d609aa1c0bd18880f77c6) disabled eslint.  driving me crazy


