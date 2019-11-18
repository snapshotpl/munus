# Munus

[![Minimum PHP Version](https://img.shields.io/badge/php-%3E%3D%207.2-8892BF.svg)](https://php.net/)
[![buddy pipeline](https://app.buddy.works/akondas/munus/pipelines/pipeline/220416/badge.svg?token=f043fc3d0fb3414a7b5c2cff118b2a43cc1e39f64b155c73661e03bb4b0d6fb9 "buddy pipeline")](https://app.buddy.works/akondas/munus/pipelines/pipeline/220416)
[![Latest Stable Version](https://poser.pugx.org/akondas/munus/v/stable?format=flat)](https://packagist.org/packages/akondas/munus)
[![CodeFactor](https://www.codefactor.io/repository/github/akondas/munus/badge)](https://www.codefactor.io/repository/github/akondas/munus)
[![Maintainability](https://api.codeclimate.com/v1/badges/4b9585a0fb57553737d5/maintainability)](https://codeclimate.com/github/akondas/munus/maintainability)
[![Total Downloads](https://poser.pugx.org/akondas/munus/downloads?format=flat)](https://packagist.org/packages/akondas/munus)
![GitHub](https://img.shields.io/github/license/akondas/munus)

Power of object-oriented programming with the elegance of functional programming.
Increase the robustness with reduced amount of code.

At the moment, in the experimental phase.

Due to the lack of generic types, Munus achieves genericity with the help of [Psalm](https://github.com/vimeo/psalm) `template` annotation.

Munus examples:
```php
/** @var Stream<int> $stream */
$stream = Stream::range(1, 10)->map(function(int $int): int {return $int * 5});

/** @var Option<Success> $option */
$option = Option::of(domainOperation());

/** @return Either<Failure,Success> */
function domainOperation(): Either {}

/** @var Trƴ<Result> $result */
$result = Trƴ::of(function(){throw new \DomainException('use ddd');});
$result->getOrElse(new Result())
```

The goal is to help achieve:
**Psalm was able to infer types for 100% of the codebase**

### Features

 - Try
 - Either
 - Option
 - Lazy (implemented as immutable linked list)
 - Stream (implemented as lazy linked list)
 - [Set](collection/set.md)
 - Lisт
 - Iterator
 - Value