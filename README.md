[Jasmine doc site](https://jasmine.github.io/)

Contributing
=================

_Note_: The files in the `_api` directory are generated by `jsdoc`. Don't edit them by hand. If you do, your changes will be overwritten the next time somebody generates them.

1. Fork the repo
1. Create your feature branch (`git checkout -b my-new-docs`)
1. Ensure ruby and bundler (`gem install bundler`) are installed
1. Install ruby dependencies (`bundle`)
 1. You can install them in the local folder, instead of globally for the system with (`bundle install --path vendor/bundle`)
1. Install pygments (`pip install pygments`) - would need python and pip (http://pygments.org/)
1. Install JS dependencies (`npm install`)
1. Make your modifications
 1. API docs are generated from the jasmine-core source files, update them with `bundle exec rake update_edge_jasmine`
 1. Run `npm run jsdoc` to regenerate jsdoc pages from .js files.
 1. Tutorials are in the `_tutorials` directory
  1. Basic markdown files go directly in `_tutorials`
  1. Docco style (side-by-side) documents should live in `_tutorials/src`
  1. Docco tutorials are generated with `bundle exec rake tutorials`
1. Preview your changes (`bundle exec jekyll serve --baseurl ''`)
1. Commit your changes (`git commit -am 'Add some docs'`)
1. Push to the branch (`git push origin my-new-docs`)
1. Create new Pull Request
