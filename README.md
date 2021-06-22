# Dumper
is a debugging tool for everyone!
---

### Feature
- array tree viewer
- dump and die

![image](https://user-images.githubusercontent.com/37282871/122924228-20941f00-d398-11eb-93c7-f9a116378513.png)
---

### Guide
- include dumper to your project
- create a helper function dd() or any name
- paste this:
```php
if (!function_exists('dd')) {
    /**
     * dump and die
     * 
     */
    function dd()
    {
        echo call_user_func_array(['App\\Core\\Dumper', 'dump'], func_get_args());
        die();
    }
}
```
---
### Usage example
```php
$router->get('/test', function () {
    $userData = DB()->selectLoop('*', 'users');
    dd($userData, $_SERVER, $_SESSION);
});
```
