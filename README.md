<h1 align="center"> laravel-admin simplemde 编辑器 </h1>

<p align="center">支持粘贴，拖拽图片上传</p>


## Installing

```shell
$ composer require vasar/simplemde-support-uploadimage

$ php artisan vendor:publish --provider=Vasar\Simplemde\SimplemdeServiceProvider
```

## Usage
In the extensions section of the config/admin.php file
```
'extensions' => [

    'simplemde' => [

        // Set to false if you want to disable this extension
        'enable' => true,

        // If you want to set an alias for the calling method
        //'alias' => 'markdown',

        // Editor configuration
        'config' => [

        ]
    ]
]
```

The configuration of the editor can be found in [Simplemde Documentation](https://github.com/sparksuite/simplemde-markdown-editor#configuration) and configuration upload image.

'config' => [
    'autofocus'   => true,
    'spellChecker' => false,
    'upload' => 'upload url',
    'uploadFieldName' => 'xxx_filedName', // 上传字段 默认：image
    'jsonFieldName' => 'xxx_jsonFieldName', // json 返回字段 默认：image
    
    ....
]

## License

MIT
