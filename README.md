# neovim

```sh
git clone --depth=1 https://github.com/mrbeardad/SpaceVim ~/.SpaceVim
ln -svf ~/.SpaceVim ~/.config/nvim
ln -svf ~/.SpaceVim/mode ~/.SpaceVim.d
g++ -O3 -std=c++11 -o ~/.local/bin/quickrun_time ~/.SpaceVim/custom/quickrun_time.cpp
# 启动neovim后执行 :SPInstall  安装插件
nvim
# 构建YCM代码补全引擎，如果需要其他语言的语义补全，见 ./install.py --help
cd ~/.cache/vimfiles/repos/github.com/ycm-core/YouCompleteMe/
./install.py --clangd-completer --go-completer
# 修改ALE语法检测引擎
cp -vf ~/.SpaceVim/custom/clangtidy.vim ~/.cache/vimfiles/repos/github.com/dense-analysis/ale/ale_linters/cpp/clangtidy.vim
```
