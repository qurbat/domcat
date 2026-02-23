# domcat

A single-file UI for categorising domains.

## Features

- Import domains from simple list or CSV
- Categorise domains individually or in bulk
- Filter by category or TLD (with proper multi-level TLD support like .co.uk, .com.au)
- Search domains with flexible options (ignore TLD, starts-with matching)
- No setup, runs entirely in the browser

## Usage

Open `domcat.html` in a web browser.

## Import formats

**Simple list:**
```
example.com
example.org
example.net
[...]
```

**List with category column:**
```
example.com,CTRL
google.com  # lines without categories are treated as uncategorised
facebook.com,GRP
[...]
```

**Compiled blocklist from [Poisoned Wells](http://github.com/qurbat/dnsblocks.in):**
```
domain,category,tranco_rank,ACT,AIRTEL,CONNECT,JIO,MTNL,YOU
0-123movies.com,MOV,-,0,1,0,0,0,0
[...]
```

Formats are automatically detected and preserved during export.

## Uncategorised domains

Domains with `UNCAT` in the category column (`example.com,UNCAT`) or in the simple list format (`example.com`) are treated as uncategorised.

## TLD support

The application properly handles multi-level TLDs using the [Public Suffix List](https://publicsuffix.org).

## Browser compatibility

This tool requires a modern browser.
