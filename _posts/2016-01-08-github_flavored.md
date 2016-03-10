---
layout: post
title:  "Github markdown"
date:   2016-01-08 11:55:03
---

Variable FOO_BAR_BAZ `FOO_BAR_BAZ`

auto link http://jekyllrb.com

~~strike~~

```js
// override the angular exception handler service.
// http://blog.loadimpact.com/blog/exception-handling-in-an-angularjs-web-application-tutorial/
offirmo_app.global_ng_module.config(['$provide', function($provide) {
	$provide.decorator('$exceptionHandler', ['$log', '$delegate', function($log, $delegate) {
			return function(exception__foo__bar, cause) {
				//console.log(arguments);
				$log.error.apply($log, arguments);

				var p = document.createElement('p');
				p.textContent = 'XXA ' + exception.message;
				window.offirmo_loader.error_console.appendChild(p);

				$delegate(exception, cause);
			};
		}
	]);
}]);
```

good bye...

