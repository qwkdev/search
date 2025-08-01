# QSearch
Fully customisable, ultra lightweight, fuzzy search util
To use, create a userscript which calls `init()` and passes in an array of modules/module urls.

EG:
```
init([
    "https://raw.githubusercontent.com/qwkdev/search/refs/heads/main/utils.json",
	{
		"google": {
			"": "https://www.google.com/",
			"*": "https://www.google.com/search?q=$*"
		}
	}
]);
```

### Example module

```
{
	"yt": {
		"search": "https://youtube.com/results?search_query=$*",
		"channel": {
			"me": "https://youtube.com/@qwkq",
			"*": "https://youtube.com/@$*",
			"": "https://youtube.com/@qwkq"
		},
		"*": "https://youtube.com",
		"": "https://youtube.com"
	},
	"g": {
		"*": "https://www.google.com/search?q=$*",
		"": "https://www.google.com"
	}
}
```

- Use $1, $2, etc for parameters
- Use $* for everything unmatched
- Put a `.` after the dollar sign for the raw parameter (Not URIencoded)
Eg: $.1, $.2, etc, or $.*
