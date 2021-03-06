# Build Your Own Sinatra

The source for the [Build Your Own Sinatra](https://buildYourOwnSinatra.com) ebook

## Building The Book

First install the gems:

```sh
$ bundle install
```

And kindlegen:

```sh
$ brew install homebrew/binary/kindlegen
```

Then install wkhtmltopdf:

On OS X:

```sh
$ brew install wkhtmltopdf
```

On Ubuntu:

```sh
$ sudo apt-get install wkhtmltopdf
```

See https://github.com/pdfkit/pdfkit/wiki/Installing-WKHTMLTOPDF for other platforms

To build html:

```sh
$ bundle exec rake build:html
```

PDF:

```sh
$ bundle exec rake build:pdf
```

EPUB:

```sh
$ bundle exec rake build:epub
```

Mobi:

```sh
$ bundle exec rake build:mobi
```

## Testing

For the tests to pass you must first build the HTML version of the book:

```sh
$ bundle exec middleman build
```

Then run rspec:

```sh
$ bundle exec rspec
```

## Live Coding

The CSS is specifically adapted to be live edited using [Takana](https://github.com/mechio/takana). This comes with some drawbacks;

1. We can only use libsass features
2. Sprocket asset paths cant be shared

First install a compatible version of bourbon:

```sh
gem install bourbon -v 3.2.4
```

Then when booting takana pass the path for the bourbon's sass to it:

```sh
takana . -i ~/.rbenv/versions/2.1.5/lib/ruby/gems/2.1.0/gems/bourbon-3.2.4/dist
```

## Help/Resources

You can get help from the following places:

- [@k_2052](http://twitter.com/k_2052) Feel free to mention me on twitter for quick questions
- [k@2052.me](mailto:k@2052.me) Email for longer questions or for communicating private information
- [Issues](https://github.com/BuildYourOwnSinatra/book/issues) File an issue for any requests, suggestions, edits, fixes etc

## Contributing

1. Fork. it
2. Create. a new branch (git checkout -b cat-evolver)
3. Commit. your changes (git commit -am 'Add Cat Evolution')
4. Test. your changes (always be testing) (you can skip this step for content changes)
5. Push. to the branch (git push origin cat-evolver)
6. Pull. Request. (for extra points include funny gif and or pun in comments)

To remember this you can use the easy to remember and totally not tongue-in-check initialism:
FCCTPP.

I don't want any of these steps to scare you off. If you don't know how to do something or are struggle getting it to work feel free to create a pull request or issue anyway. I'll be happy to help you get your contributions up to code and into the repo!

## License

Licensed under MIT for your convenience. Quote from it, reuse it, remix etc in any way you like. The only rule is the golden one; don't do anything with my book you wouldn't want someone to do with yours.
