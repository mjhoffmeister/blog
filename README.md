# Local setup

## Windows

### Environment setup

1. Install [Ruby+Devkit](https://rubyinstaller.org/downloads/)
2. Run the `ridk install` step when prompted in the last stage of the installer
3. Choose `MSYS2 and MINGW development toolchain` in the command prompt that opens (option 3 as of
this writing)
4. Open a new command prompt to get PATH updates
5. Execute `gem install jekyll bundler`
6. In the project root folder, run `bundle update github-pages`
7. If you get a message about an error occurring while installing `wdm`, run `gem install wdm:0.1.1 
-- --with-cflags=-Wno-implicit-function-declaration`
8. Execute `bundle exec jekyll -v` to verify your Jekyll installation

### Running locally

After your environment is configured, execute the following command to run locally.

`bundle exec jekyll serve`