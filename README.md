# resize_image_in_laravel
Resize your image before uploading 

first of all exicute given command on your project directory using composer 

composer require intervention/image

after successful installation 

After you have installed Intervention Image, open your Laravel config file config/app.php and add the following lines.

Intervention\Image\ImageServiceProvider::class

Add the facade of this package to the $aliases array.

'Image' => Intervention\Image\Facades\Image::class

Configure using 
php artisan vendor:publish --provider="Intervention\Image\ImageServiceProviderLaravelRecent"


Usage:


// usage inside a laravel route
Route::get('/', function()
{
    $img = Image::make('foo.jpg')->resize(300, 200);
    return $img->response('jpg');
});
