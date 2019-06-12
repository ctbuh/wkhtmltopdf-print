# wkhtmltopdf-print

### Builds


https://cdn.jsdelivr.net/gh/ctbuh/wkhtmltopdf-print/dist/bs4-print.css

https://cdn.jsdelivr.net/gh/ctbuh/wkhtmltopdf-print/dist/bs3-print.css

Best optimized look

```php
$options = array(
    'viewport-size' => '1024x768',

    'no-outline' => true,
    'print-media-type' => true,
    'disable-javascript' => true,

    'margin-top' => '1cm',
    'margin-right' => '0.5cm',
    'margin-bottom' => '0.5cm',
    'margin-left' => '0.5cm',

    'page-size' => 'A4',
    'dpi' => 96, // 72
    'cache-dir' => storage_path('cache_pdf')
);

$snappy->setOptions($options);
```


## Optimization Notes
- fontconfig cache was stale and as a non privileged user, fontconfig was unable to write it to /var/cache/fontconfig,
- inline css instead of making additional HTTP requests
- disable IPv6 and use HTTP instead of HTTPS
- reduce default DPI to 72
- remove all custom fonts
- remove all @import rules
- enable and use cache-dir option

Install missing packages:
```
sudo apt-get install -y openssl build-essential xorg libssl-dev openssl-devel
```

### Links
- https://github.com/wkhtmltopdf/wkhtmltopdf/issues/1510
- http://perfectionkills.com/profiling-css-for-fun-and-profit-optimization-notes/


