# Hugo Learn Theme

To add this theme as a submodule run the following:

    git submodule add -- https://github.com/jshook/hugo-theme-learn.git ./themes/hugo-theme-learn

The submodule will get pulled into a new directory in your repo:

```
themes
└── hugo-theme-learn
    ├── LICENSE.md
    ├── PERHAPS.md
    ├── README.md
...
```

Do not edit files directly in the `themes` directory, changes to the theme should happen in this repo and then propagated to existing repos that use this one as a submodule. To propagate changes navigate to the `themes/hugo-theme-learn directory` and run git pull. Then you will have to add / commit / and push the `themes/hugo-theme-learn directory` to commit the update to your repo.

***NOTE*** When using this as a git submodule in your themes directory, you may have to run this command from your top level git directory:
~~~
git submodule update --init
~~~


This repository contains a theme for [Hugo](https://gohugo.io/), based on great [Grav Learn Theme](http://learn.getgrav.org/).

Visit the [theme documentation](https://matcornic.github.io/hugo-learn-doc/basics/what-is-this-hugo-theme/) to see what is going on. It is actually built with this theme.

## vi/vim settings

If you use vim or a vim-backed vi editor, you might prefer these settings to prevent hugo from trying to render unrelated partial content from vim swap files an backups. You can simply add these to your ~/.vimrc
~~~
set backup
set backupdir=~/.vim/tmp
set dir=~/.vim/tmp
~~~
If you use these settings, be sure to
~~~
mkdir -p ~/.vim/tmp
~~~


## Installation
Navigate to your themes folder in your Hugo site and use the following commands:
```
$ cd themes
$ git clone https://github.com/matcornic/hugo-theme-learn.git
```

Check that your Hugo version is minimum `0.19` with `hugo version`.

![Overview](https://github.com/matcornic/hugo-theme-learn/raw/master/images/tn.png)

## Usage

- [Visit the documentation](https://matcornic.github.io/hugo-learn-doc/basics/what-is-this-hugo-theme/)

# Main functionalities

- Handle two levels of documentation
- Tip/Note/Info and Warning boxes
- Resize images
- Preview of original image size
- Add shadow or border on images
- Automatic table of contents
- Create buttons (typically used to provide a link to a demo)
- Search using `lunr` index

# TODO

- [Handling more than 2 levels in documentation](https://github.com/matcornic/hugo-theme-learn/issues/11)
- [Handling videos](https://github.com/matcornic/hugo-theme-learn/issues/13)
- [Add optional button to create doc issue (like github)](https://github.com/matcornic/hugo-theme-learn/issues/14)

# Troubleshooting

Changes have been made for automatically creating previous and next arrows. These changes restructured the theme and you might have compatibility problems when updating to the latest version of the theme. Please read [PR#36](https://github.com/matcornic/hugo-theme-learn/pull/36) to update your documentation with latest guidelines.

If you don't want to update your documentation, use the git tag `1.0.0` 

```shell
cd themes/hugo-theme-learn
git checkout tags/1.0.0
```
