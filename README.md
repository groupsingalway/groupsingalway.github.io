<!-- omit in toc -->
# groupsingalway.io

- [Structure](#structure)
	- [Files in the main directory](#files-in-the-main-directory)
	- [Subdirectories](#subdirectories)
- [Contributing](#contributing)
	- [Editing a conference posting](#editing-a-conference-posting)
	- [Building](#building)

## Structure

We will briefly go through the basic structure of the repository here.

### Files in the main directory

Basic information for the website is included in the `_config.yml` file. Information that does not change from year to year should probably be included in this file. 

The `Gemfile` has relevant information for [Ruby](https://www.ruby-lang.org/en/). One does not need Ruby to make changes to the build files; see [Contributing](#contributing).

There are a few `html` files at the top level; these are used to build `html` files for the website. Although they are `html` files, they can interpret markdown and [Liquid](https://jekyllrb.com/docs/liquid/). 

### Subdirectories

Ther are two types of subdirectories: those beginning with `_` and those that do not. Those directories starting with `_` are purely build files. Those directories without `_` are transferred directly to the website. 

The `docs` directory *is* the website. That is, GitHub looks in `docs/` for the website files. This puts the compilation on us rather than GitHub; this was necessary based on the Jekyll-style of the website. I hope to change this soon, so that GitHub compiles everything, removing our need for the `docs/` subdirectory.

## Contributing

There are three types of editing the website.
1. Editing the files that are used to build the website.
2. Changing the html files of the website.
3. Email the suggestions to Josh.

To make changes of the second type, one needs [Ruby](https://www.ruby-lang.org/en/). See [Building](#building) for details on how to build the website yourself; this enables one to view the changes locally as well.

### Editing a conference posting

Conference websites are written in markdown in the `collections/_posts` subdirectory. This is modeled off of blogging sites, so files are modeled with the `YYYY-MM-DD-Name.md` format. The website will order the postings in chronological order.

### Building 

Assuming Ruby is installed, run 
```ruby
bundle install
```

This will install a number of gems, and once that is successful, the website can be *served* (viewed locally) or *built*.

To build the website run 
```ruby
bundle exec jekyll build
```

The website is built to the `_site` directory. You can simply run
```bash
rm -r docs 
mv _site docs
```

To view the website, rather than build, run 
```ruby
bundle exec jekyll serve
```