## How to start

1. `git clone git@github.com:mrtaddy/tech-octopress.git`
1. `cd tech-octopress`
1. `bundle install`
1. `git clone git@github.com:mrtaddy/omg-tech.git _deploy`

## How to write blog post

1. `bundle exec rake new_post[Post Title]`
1. Write contents to `source/_posts/YYYY-MM-DD-post-title.markdown`
1. `bundle exec rake preview` and view http://localhost:4000/
1. `git add . && git ci -m "Add new post"`
1. `bundle exec rake deploy`

## Documentation

Check out [Octopress.org](http://octopress.org/docs) for guides and documentation.

## Octopress Original License
(The MIT License)

Copyright © 2009-2013 Brandon Mathis

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the ‘Software’), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED ‘AS IS’, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
