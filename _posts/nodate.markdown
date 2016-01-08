---
layout: post
title:  "does it work without date ?"
date:   2016-01-08 11:55:03
categories: foo
---
You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve --watch`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight javascript %}
	// override the angular exception handler service.
	// http://blog.loadimpact.com/blog/exception-handling-in-an-angularjs-web-application-tutorial/
	offirmo_app.global_ng_module.config(['$provide', function($provide) {
		$provide.decorator('$exceptionHandler', ['$log', '$delegate', function($log, $delegate) {
				return function(exception, cause) {
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
{% endhighlight %}

Check out the [Jekyll docs][jekyll] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll’s dedicated Help repository][jekyll-help].

[jekyll]:      http://jekyllrb.com
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-help]: https://github.com/jekyll/jekyll-help
