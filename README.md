Slick Widget
============================

The Slick is a Yii2 wrapper for the [Slick] (https://kenwheeler.github.io/slick/)

[![Latest Stable Version](https://poser.pugx.org/anix/wgt-owlcarousel/v/stable.svg)](https://packagist.org/packages/anix/wgt-owlcarousel)
[![Total Downloads](https://poser.pugx.org/anix/wgt-owlcarousel/downloads.svg)](https://packagist.org/packages/anix/wgt-owlcarousel)


Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
php composer require --prefer-dist panix/wgt-slick "*"
```

or add

```
"panix/wgt-slick": "*"
```

to the require section of your `composer.json` file.

Usage
-----

Once the extension is installed, simply use it in your code by  :

```php
<?php
use panix\ext\slick\SlickWidget;

SlickWidget::begin([
    'containerTag' => 'div',
    'containerOptions' => [
        'class' => 'container-class'
    ],
    'options'    => [
        'autoplay'          => true,
        'autoplayTimeout'   => 3000,
        'items'             => 3,
        'loop'              => true,
        'responsiveClass' => true,
        'responsive' => [
            0 => [
                'items' => 1,
                'nav' => false,
                'dots' => true,
                'center' => true,
            ],
            426 => [
                'items' => 2,
                'nav' => false
            ],
            768 => [
                'items' => 2,
                'nav' => false
            ],
            1024 => [
                'items' => 5,
                'nav' => true,
                'dots' => false
            ]
        ]
    ]
]);
?>

<div class="item-class"><img src="/img/1.jpg" alt="Image 1"></div>
<div class="item-class"><img src="/img/2.jpg" alt="Image 2"></div>
<div class="item-class"><img src="/img/3.jpg" alt="Image 3"></div>
<div class="item-class"><img src="/img/4.jpg" alt="Image 4"></div>


<?php SlickWidget::end(); ?>
