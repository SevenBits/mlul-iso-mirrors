Mac Linux USB Loader ISO Mirror Repository
=========

Hey everyone. This repository is kind of special. As I [mentioned in one of my blog posts](http://sevenbits-tech-blog.blogspot.com/2014/05/mac-linux-usb-loader-declassified.html), I want to expand the distribution downloader in Mac Linux USB Loader so that it downloads from a variety of mirror sites instead of just one hard-coded URL. This is advantageous for a number of reasons:

  1. The process is more convenient and fast for end users, as you can download from the server closest to you.
  1. It is easier on bandwidth, as users can choose from many servers instead of just one, lightening the load on each server.
  1. It is more community-orientied, because now everyone can contribute.

This repository is structured so that the `mirrors` folder contains JSON files, one for each distribution supported by Mac Linux USB Loader. Because the distribution downloader will only support downloading the *latest version* of each supported distribution, maintenence will simply involve updating the JSON files at each new release of a supported distribution. Here's an example of the Linux Mint JSON file, `Linux-Mint.json`:

```JSON
{
  "mirrors": [
    {
      "url": "http://mirror.metrocast.net/linuxmint/stable/16/linuxmint-16-cinnamon-dvd-64bit.iso",
      "name": "MetroCast Cablevision",
      "countryLong": "United States of America"
    },
  ],
  "imageURL": "http://www.example.com/test.jpg"
}
```

Each JSON file will be named in the following way:

 - All spaces in the name will become dashes (so, `Linux Mint` becomes `Linux-Mint`)
 - The extension `.json` will be appended to the end of the name.
 - The file will be placed in the `mirrors` folder.

Contributions
----

Obviously, it's going to take a lot of work maintaining this. So, I would love and greatly welcome community participation. So, to help out, [fork this repository](https://github.com/SevenBits/mlul-iso-mirrors/fork) and in your fork, add any new files that are needed to support supported distributions, register some mirrors with JSON, and submit a pull request. Thanks!

Supported Distributions
----

 - Ubuntu
 - Linux Mint
 - Elementary OS
 - Zorin OS
 - Kali (not *quite* working yet, but getting there)

License
----

See the included `LICENSE` file.