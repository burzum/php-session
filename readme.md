# Agnostic php session library

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)
[![Scrutinizer Coverage](https://img.shields.io/scrutinizer/coverage/g/Phauthentic/session/master.svg?style=flat-square)](https://scrutinizer-ci.com/g/Phauthentic/session/)
[![Code Quality](https://img.shields.io/scrutinizer/g/Phauthentic/session/master.svg?style=flat-square)](https://scrutinizer-ci.com/g/Phauthentic/session/)

A framework agnostic session library with convenient dot notation access.

## Example

This is a very simple example to give you an idea of how to use it:

```php
use Phauthentic\Session\Session;
use Phauthentic\Session\Config as SessionConfig;

$config = (new SessionConfig())
    ->setSessionName('my-app')
    ->setGcMaxLifeTime(60);

$session = new Session($config);
$session->write('user', ['username' => 'foo']);

echo $session->read('user.username');
```

## Copyright & License

Licensed under the [MIT license](LICENSE.txt).

* Copyright (c) Florian Krämer
* Copyright (c) [Cake Software Foundation, Inc.](https://cakefoundation.org)
