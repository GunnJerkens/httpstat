# httpstat

Easily check the HTTP status of a list of URLs.

## installation

Put `httpstat` somewhere in your path, such as `/usr/local/bin/`, or call it
with the path, such as `./httpstat`.

Requires `curl` and `perl`.

## usage

    httpstat [-v] [urls...]

You can also pipe in a list of URLs on separate lines:

    cat urls.txt | httpstat

For example, this input:

    google.com
    www.google.com

gives this output:

    301 google.com -> http://www.google.com/
    200 www.google.com

The tool is lazy, showing redirects but not following them. You will probably
want to update your list with the URL after `->` in the response.

## options

`-v` **verbose**: print out all headers received for each domain.

## license

MIT
