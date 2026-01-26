## 🛠️ Setup
### Install Jekyll on Ubuntu
Prerequisites
```text
Jekyll requires the following:
- Ruby version 2.7.0 or higher
- RubyGems
- GCC and Make
```
Install Ruby and other prerequisites
```bash
sudo apt-get install ruby-full build-essential zlib1g-dev
```
Set up a `gem` installation directory for you user account
```bash
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
Install Jekyll and Bundler
```bash
gem install jekyll bundler
```
That’s it! You’re ready to start using Jekyll.
> [!NOTE]
> How to install jekyll  
> [Installation about jekyll(offcial)](https://jekyllrb.com/docs/installation/)

> [!NOTE]
> How to install Bundler
> [Bundler (offcial)](https://bundler.io/)

## 🎮 Usage
### Building and previewing your site locally
1. Change your working directory to the root directory of your site.
2. Run `bundle install`
```bash
bundle install
```
3. Run `bundle exec jekyll serve` to build your site and preview it at `localhost:4000`.\\
   The built site is stored in the directory `_site`.
```bash
bundle exec jekyll serve
```

## 📚 References
- [jekyll (Official)](https://jekyllrb-ja.github.io/)
- [Jekyll Themes (Official)](https://jekyllthemes.io/)
- [Just the Docs (Official)](https://just-the-docs.com/)