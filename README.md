# Jasmine JUnitReporter

A [Jasmine 2][j2] reporter that outputs JUnit 4.x compatible
results. Designed for use in CI environments that use
[PhantomJS][phantom] to run Jasmine specs.

[j2]: http://jasmine.github.io/2.0/introduction.html
[phantom]: http://phantomjs.org/

## Installation

Download the file and place it with the rest of your Jasmine scripts.

## Usage

Add the reporter to your Jasmine runner HTML:

```html
<script src="scripts/JUnitReporter.js"></script>
<script src="scripts/JUnitReporter.boot.js"></script>
```

`JUnitReporter.boot.js` is the glue code you need to provide to
configure and enable the reporter. It should look something like:

```js
(function() {
  var reporter = new jasmine.JUnitReporter({
    outputDir: 'output/dir'
  });
  jasmine.getEnv().addReporter(reporter);
})();
```

## Contributing

1. Fork it ( http://github.com/shepmaster/jasmine-junitreporter/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
