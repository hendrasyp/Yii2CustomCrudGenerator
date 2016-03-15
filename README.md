# Yii2CustomCrudGenerator
Konfigurasi untuk membuat Custom Crud Generator

## Configuration
### First Step
#### @app/config/web.php
```<?php

if (YII_ENV_DEV) {
    // configuration adjustments for 'dev' environment
  $config['bootstrap'][] = 'debug';
  $config['modules']['debug'] = [
    'class' => 'yii\debug\Module',
		'allowedIPs' => ['127.0.0.1'],
  ];

  $config['bootstrap'][] = 'gii';
  $config['modules']['gii'] = [
    'class' => 'yii\gii\Module',
    'generators' => [
      'crud' => [
				'class' => 'yii\gii\generators\crud\Generator',
				'templates' => ['mycustoms' => '@app/components/Generators/crud/mycustoms']
			] // end of crud
		],
  ];
}

return $config; ?> 
```
### Last
Copy this repository to component's directory

### How it works ?
Go to gii, create some or one crud, and see the result :)
