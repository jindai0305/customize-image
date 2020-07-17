# Description
customize image by php-gd
# install
```
composer require jingdai/customize-image
```
# Usage
```php
use Jindai\Draw;

------

$im = new Draw();
$im->createBgWithColor(200, 200, '#000000');
// or
// $im->createBgWithFile('https://t.g.mg-cdn.com/uploads/static/8/201904/up_5cb419c6485d71.85611243.jpg/thumb-2-170');
$im->color = '#000000';
$im->float = 'right';
$im->addText('雷宇笛', 100, 20);
$im->addRadiusImage('https://t.g.mg-cdn.com/uploads/static/8/201904/up_5cb419c6485d71.85611243.jpg/thumb-2-170', 50, 50, 50, 50, 50);

return response($im->toPng(), 200, ['Content-Type' => 'image/png',]);
```
# License
The Easy - Excel is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT)
