# DEVELOPMENT

This project uses [jekyll](https://jekyllrb.com/), a static site generator written in ruby.

1. Install [`rtx`](https://github.com/jdxcode/rtx) (which we will then use to install ruby).

   ```shell
   curl https://rtx.pub/rtx-latest-macos-arm64 > ~/bin/rtx
   chmod +x ~/bin/rtx
   rtx --version
   echo 'eval "$(~/bin/rtx activate zsh)"' >> ~/.zshrc
   source ~/.zshrc
   ```

2. Install `ruby` version 3 (currently latest major version).

   ```shell
   rtx install ruby@3
   ```

3. Install [`jekyll`](https://jekyllrb.com/) version [4.2.2](https://rubygems.org/gems/jekyll/versions/4.2.2) which is the last version that continues [libass](https://github.com/sass/libsass) which is [now deprecated](https://sass-lang.com/blog/libsass-is-deprecated/) in favor of [dart-sass](https://sass-lang.com/dart-sass/). Using this older version of libsass prevents any deprecation warnings.

   ```shell
   gem install jekyll -v 4.2.2
   jekyll serve
   ```
