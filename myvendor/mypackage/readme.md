# MyPackage

[![Latest Version on Packagist][ico-version]][link-packagist]
[![Total Downloads][ico-downloads]][link-downloads]
[![Build Status][ico-travis]][link-travis]
[![StyleCI][ico-styleci]][link-styleci]

This is where your description should go. Take a look at [contributing.md](contributing.md) to see a to do list.

## Installation

Via Composer

``` bash
$ composer require myvendor/mypackage
```

## How to Use
### publish vendor :
$ php artisan publish:vendor

### Use trait Show in your controller :
  namespace App\Http\Controllers\Admin;
  
  use MyVendor\MyPackage\Traits\Show;
  
  class YourCrudController extends CrudController
  {
    use Show;
  }
  
  
### Add this in your controller :
        $this->crud->setListView('myvendor::modal.list');

        $this->crud->modifyButton('update',[
            'content' => 'myvendor::buttons.update',
        ]);

### Create route to function of trait Show in custom.php:
        Route::get('user/add', 'UserCrudController@create'); // Create {{ user}} route
        Route::get('user/update/{id}', 'UserCrudController@edit'); // Update {{ user }} route
        CRUD::resource('user','UserCrudController');
        
## Change log

Please see the [changelog](changelog.md) for more information on what has changed recently.

## Testing

``` bash
$ composer test
```

## Contributing

Please see [contributing.md](contributing.md) for details and a todolist.

## Security

If you discover any security related issues, please email author email instead of using the issue tracker.

## Credits

- [author name][link-author]
- [All Contributors][link-contributors]

## License

license. Please see the [license file](license.md) for more information.

[ico-version]: https://img.shields.io/packagist/v/myvendor/mypackage.svg?style=flat-square
[ico-downloads]: https://img.shields.io/packagist/dt/myvendor/mypackage.svg?style=flat-square
[ico-travis]: https://img.shields.io/travis/myvendor/mypackage/master.svg?style=flat-square
[ico-styleci]: https://styleci.io/repos/12345678/shield

[link-packagist]: https://packagist.org/packages/myvendor/mypackage
[link-downloads]: https://packagist.org/packages/myvendor/mypackage
[link-travis]: https://travis-ci.org/myvendor/mypackage
[link-styleci]: https://styleci.io/repos/12345678
[link-author]: https://github.com/myvendor
[link-contributors]: ../../contributors
