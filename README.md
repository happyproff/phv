Switch PHP version on Debian-based systems with update-alternatives under the hood.

## Usage

`$ php -v`

```
PHP 8.3.12 (cli) (built: Sep 27 2024 03:53:05) (NTS)
...
```

`$ phv`

```shell
Selected:
8.3.12

Available:
7.3
7.4
8.0
8.1
8.2
8.3
8.4

To select another version, specify it like this:
  phv 8.2
```

`$ phv 8.2`

```
[sudo] password for user: 
update-alternatives: using /usr/bin/php8.2 to provide /usr/bin/php (php) in manual mode
update-alternatives: using /usr/bin/phar8.2 to provide /usr/bin/phar (phar) in manual mode
update-alternatives: using /usr/bin/phar.phar8.2 to provide /usr/bin/phar.phar (phar.phar) in manual mode

Selected:
8.2.24
```

`$ php -v`

```
PHP 8.2.24 (cli) (built: Sep 27 2024 04:04:39) (NTS)
...
```

## Installation

### user
```shell
git clone git@github.com:happyproff/phv.git

cp phv/phv ~/.local/bin/phv
# or
ln -s "$(pwd)/phv/phv" ~/.local/bin/phv
```

### global
```shell
git clone git@github.com:happyproff/phv.git

sudo cp phv/phv /usr/local/bin/phv
```
