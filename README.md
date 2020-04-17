foaas-python
============

A simple Python library to [FOAAS].

[![build status](https://secure.travis-ci.org/dmpayton/foaas-python.png)](http://travis-ci.org/dmpayton/foaas-python)
[![test coverage](https://coveralls.io/repos/dmpayton/foaas-python/badge.png)](https://coveralls.io/r/dmpayton/foaas-python)
[![downloads](https://pypip.in/d/foaas/badge.png)](https://crate.io/packages/foaas/)

* **Author**: [Derek Payton]
* **Version**: 0.2.0
* **License**: [MIT]

Documentation
-------------

### Installation

This package relies on [requests] and should be installed with [pip]:

```
pip install foaas
```

### Basic Usage

Fuck off:

```
>>> from foaas import fuck
>>> fuck.off(name='Tom', from_='Chris').text
Fuck off, Tom. - Chris
```

Give me some fucking JSON:

```
>>> fuck.that(from_='Chris').json
{u'message': u'Fuck that.', u'subtitle': u'- Chris'}
```

Just get the fucking URL:

```
>>> fuck.everything(from_='Chris').url
http://foaas.herokuapp.com/everything/Chris
```

This needs to be fucking secure:

```
>>> from foaas import Fuck
>>> fuck = Fuck(secure=True)
>>> fucking = fuck.life(from_='Phil')
>>> fucking.url
https://foaas.herokuapp.com/life/Phil
>>> fucking.text
Fuck my life. - Phil
```

Give me some random fucking things:

```
>>> fuck.random(from_='Chris').text
Fuck you very much. - Chris
>>> fuck.random(from_='Chris').text
Fuck my life. - Chris
>>> fuck.random(name='Tom', from_='Chris').text
Fuck me gently with a chainsaw, Tom. Do I look like Mother Teresa? - Chris
>>> fuck.random(name='Tom', from_='Chris').text
Fuck off, Tom. - Chris
```

### Supported Actions

 * `fuck.awesome(from_)`
 * `fuck.ballmer(name, company, from_)`
 * `fuck.because(from_)`
 * `fuck.bus(name, from_)`
 * `fuck.bye(from_)`
 * `fuck.caniuse(namer, from_)`
 * `fuck.chainsaw(name, from_)`
 * `fuck.cool(from_)`
 * `fuck.diabetes(from_)`
 * `fuck.donut(name, from_)`
 * `fuck.everyone(from_)`
 * `fuck.everything(from_)`
 * `fuck.fascinating(from_)`
 * `fuck.field(name, from_, reference)`
 * `fuck.flying(from_)`
 * `fuck.king(name, from_)`
 * `fuck.life(from_)`
 * `fuck.linus(name, from_)`
 * `fuck.madison(name, from_)`
 * `fuck.nugget(name, from_)`
 * `fuck.off(name, from_)`
 * `fuck.outside(name, from_)`
 * `fuck.pink(from_)`
 * `fuck.thanks(from_)`
 * `fuck.that(from_)`
 * `fuck.thing(thing, from_)`
 * `fuck.this(from_)`
 * `fuck.random(name, from_)`
 * `fuck.shakespeare(name, from_)`
 * `fuck.what(from_)`
 * `fuck.xmas(name, from_)`
 * `fuck.yoda(name, from_)`
 * `fuck.you(name, from_)`

### tl;dr

```
foaas.Fuck([secure=True]).<action>(**kwargs)[.<url|html|text|json>]
```

Testing
-------

```
$ python tests.py
.......
----------------------------------------------------------------------
Ran 7 tests in 0.724s

OK
```

... or use [tox]:

```
$ tox
```

[FOAAS]: http://foaas.com/
[Derek Payton]: http://dmpayton.com
[MIT]: https://github.com/dmpayton/foaas-python/blob/master/LICENSE
[requests]: http://python-requests.org/
[pip]: http://www.pip-installer.org/
[tox]: https://tox.readthedocs.org/
