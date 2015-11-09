## angulartics-daum-clix-retargeting

[![NPM version][npm-image]][npm-url] [![NPM downloads][npm-downloads-image]][npm-downloads-url] [![Bower version][bower-image]][bower-url] [![Dependencies status][dep-status-image]][dep-status-url] [![MIT license][license-image]][license-url] [![Join the Slack chat][slack-image]][slack-url]

Daum Clix Retargeting plugin for [Angulartics](http://github.com/luisfarzati/angulartics).

## Install

First make sure you've read installation and setup instructions for [Angulartics](https://github.com/luisfarzati/angulartics#install).

Then you can install this package either with `npm` or with `bower`.

### npm

```shell
npm install angulartics-daum-clix-retargeting
```

Then add `angulartics.daum.clix.retargeting` as a dependency for your app:

```javascript
require('angulartics')

angular.module('myApp', [
  'angulartics', 
  require('angulartics-daum-clix-retargeting')
]);
```

> Please note that core Angulartics doesn't export the name yet, but it will once we move it into [the new organization](http://github.com/angulartics).

### bower

```shell
bower install angulartics-daum-clix-retargeting
```

Add the `<script>` to your `index.html`:

```html
<script src="/bower_components/angulartics-daum-clix-retargeting/dist/angulartics-daum-clix-retargeting.min.js"></script>
```

Then add `angulartics.daum.clix.retargeting` as a dependency for your app:

```javascript
angular.module('myApp', [
  'angulartics', 
  'angulartics.daum.clix.retargeting'
]);
```


## Changes in the Daum Clix retargeting snippet

The snippet code provided by Daum Clix does not support async pageview hit, but this is supported built-in script in angulartics-daum-clix-retarget, so make sure to delete the tracking script:

```js
<script type="text/javascript">
  var roosevelt_params = {
      retargeting_id:'NTubVj7i5Pe2XCY-e8-G6Q00',
      tag_label:'g4dlUA3IRFSvJFk8Ad2Pkw'
  };
</script>
<script type="text/javascript" src="//adimg.daumcdn.net/rt/roosevelt.js" async></script> <!-- REMOVE THIS SCRIPT! -->
```

Done. Open your app, browse across the different routes and check [the Retargeting page in Daum Clix](https://clix.biz.daum.net/retargeting/retargetingList.do) to see the hits.

## Documentation

Documentation is available on the [Angulartics site](http://luisfarzati.github.io/angulartics).

## Development

```shell
npm run build
```

## License

[MIT](LICENSE)

See full license on [mooyoul.mit-license.org](http://mooyoul.mit-license.org/)

[npm-image]: https://img.shields.io/npm/v/angulartics-daum-clix-retargeting.svg
[npm-url]: https://npmjs.org/package/angulartics-daum-clix-retargeting
[npm-downloads-image]: https://img.shields.io/npm/dm/angulartics-daum-clix-retargeting.svg
[npm-downloads-url]: https://npmjs.org/package/angulartics-daum-clix-retargeting
[bower-image]: https://img.shields.io/bower/v/angulartics-daum-clix-retargeting.svg
[bower-url]: http://bower.io/search/?q=angulartics-daum-clix-retargeting
[dep-status-image]: https://img.shields.io/david/mooyoul/angulartics-daum-clix-retargeting.svg
[dep-status-url]: https://david-dm.org/mooyoul/angulartics-daum-clix-retargeting
[license-image]: http://img.shields.io/badge/license-MIT-blue.svg
[license-url]: http://mooyoul.mit-license.org/
[slack-image]: https://angulartics.herokuapp.com/badge.svg
[slack-url]: https://angulartics.herokuapp.com