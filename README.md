# wkhtmltopdf-print

https://cdn.jsdelivr.net/gh/ctbuh/wkhtmltopdf-print/dist/bs4-print.css


best options:

```php
$pdf = PDF::loadHTML($view->render());
$pdf->setOption('viewport-size', '800x600');
$pdf->setOption('viewport-size', '1024x768');

$pdf->setOption('no-outline', true);
$pdf->setOption('print-media-type', true);
$pdf->setOption('disable-javascript', true);

$pdf->setOption('margin-top', '1cm');
$pdf->setOption('margin-right', '0.5cm');
$pdf->setOption('margin-bottom', '0.5cm');
$pdf->setOption('margin-left', '0.5cm');
//$pdf->setOption('disable-smart-shrinking', true);
$pdf->setOption('page-size', 'A4');
$pdf->setOption('dpi', 96);
```


## invoice template ideas

