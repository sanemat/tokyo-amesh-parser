# tokyo-amesh-scraper
[![Npm Version](http://img.shields.io/npm/v/tokyo-amesh-scraper.svg?style=flat)](http://badge.fury.io/js/tokyo-amesh-scraper)
[![Build Status](http://img.shields.io/travis/sanemat/tokyo-amesh-scraper/master.svg?style=flat)](https://travis-ci.org/sanemat/tokyo-amesh-scraper)
[![Code Climate](http://img.shields.io/codeclimate/github/sanemat/tokyo-amesh-scraper.svg?style=flat)](https://codeclimate.com/github/sanemat/tokyo-amesh-scraper)

Scrape image urls of `tokyo-ame.jwa.or.jp`

## Getting Started
Install the module with: `npm install tokyo-amesh-scraper`

```javascript
var TokyoAmeshScraper = require('tokyo-amesh-scraper');
var amesh = TokyoAmeshScraper();

amesh.boundaryMapURL(function(err, data){
  data;// => http://tokyo-ame.jwa.or.jp/map/msk000.png
});
amesh.landformURL(function(err, data){
  data;// => http://tokyo-ame.jwa.or.jp/map/map000.jpg
});
amesh.rainMeshURL(function(err, data){
  data;// => http://tokyo-ame.jwa.or.jp/mesh/000/201405272250.gif
});
amesh.rainMeshURLs(function(err, data){
  data;// => ['http://meshURL1', 'http://meshURL2', ...]
});
```

### One More Thing
This is high resolution.

```javascript
var TokyoAmeshScraper = require('tokyo-amesh-scraper');
var amesh = TokyoAmeshScraper({ highResolution: true });

amesh.boundaryMapURL(function(err, data){
  data;// => http://tokyo-ame.jwa.or.jp/map/msk100.png
});
amesh.landformURL(function(err, data){
  data;// => http://tokyo-ame.jwa.or.jp/map/map100.jpg
});
amesh.rainMeshURL(function(err, data){
  data;// => http://tokyo-ame.jwa.or.jp/mesh/100/201405272250.gif
});
amesh.rainMeshURLs(function(err, data){
  data;// => ['http://meshURL1', 'http://meshURL2', ...]
});
```


## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).

## Release History

### v1.0.0
- Change API argument
- Add `#rainMeshURLs` for get all rain meshes

### v0.1.0
- Adjust high resolution/ normal resolution.

## License
Copyright (c) 2014 sanemat. Licensed under the MIT license.
