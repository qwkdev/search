### Example module

```
{
	"yt": {
		"search": "https://youtube.com/results?search_query=$2"
		"channel": {
			"me": "https://youtube.com/@qwkq"
			"*": "https://youtube.com/@$2"
			"": "https://youtube.com/@qwkq"
		}
		"*": "https://youtube.com"
		"": "https://youtube.com"
	}
}
```

- Use $1, $2, etc for parameters
- Use $* for everything unmatched
- Put a `.` after the dollar sign for the raw parameter (Not URIencoded)
Eg: $.1, $.2, etc, or $.*