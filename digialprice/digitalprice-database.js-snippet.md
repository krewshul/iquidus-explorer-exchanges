## Add the following to lib/database.js at the top within the ``var`` section
```
, digitalprice = require('./markets/digitalprice')
```

## Add the following to lib/database.js in ``get_market_data`` on line 191
```
case 'digitalprice':
	digitalprice.get_data(settings.markets.coin, settings.markets.exchange, function (err, obj) {
		return cb(err, obj);
	});
	break;
```

## Add the following to locale/{lang}.json under the ``// Markets`` section
```
"digitalprice": "DigitalPrice",
```