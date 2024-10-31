# SbiTa Core
General tools that common between WpKok products.

## Use and Hooks
Add a new settings:
```php
$sbita_option = new SbitaCoreOptionModel('NEW_OPTION_NAME');
$sbita_option->setDefaultValue('DEFAULT VALUE');
$sbita_option->setDescription('DESCRIPTION');
$sbita_option->setInputType('INPUT TYPE'); // e:text, number, textarea, ...
$sbita_option->setLabel('INPUT LABEL');
$sbita_option->setGroup('CUSTOM SETTINGS');
$sbita_option->add();
```

Add a item to about page:
```php
add_filter('sbita_about_items', function($array){
$array['NEW ITEM'] = 'URL';
return $array;
});
```

Get a option value
```php
$value = sbita_get_option('KEY');
```
