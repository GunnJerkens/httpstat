# httpstat

Easily check the HTTP status of a list of URLs.

## installation

Put `httpstat` somewhere in your path, such as `/usr/local/bin/`.

## usage

Put a list of URLs in a text file, and pipe them into `httpstat`.

    cat urls.txt | httpstat

For example, this input:

    google.com
    www.google.com

gives this output:

    (301) google.com -> http://www.google.com/
    (200) www.google.com

The tool is lazy, and doesn't follow redirects, but it does show them. To get
the status of the destination of a redirect, take the URL after the `->`, and
use it to replace that line in your `urls.txt` file.

## license

MIT
