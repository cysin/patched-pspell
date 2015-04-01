# patched-pspell
Automatically exported from code.google.com/p/patched-pspell

The 'pspell' PHP extension offers only few functions to customize. This patch added 'pspell_config_set' function so that you can set any options you want.


The patch was based on PHP 5.4.6. You can open pspell.c.patch for details to make your own patch if the PHP version was not compatible.


if you have any problems pleas contact blueflycn at gmail dot com.


==install==


1. Download pspell.c.patch and put it under php-xxx/ext/pspell directory.

2. Run 'patch < pspell.c.patch' in the command line.

3. Install the patched pspell extension and enable it via php.ini


==usage==


{{{
pspell_config_set($pspell_config, 'ignore-case', 'true');
pspell_config_set($pspell_config, 'sug-mode', 'bad-spellers');
}}}


For a full reference to see what option names are available, please refer to common/config.cpp in the aspell source package, the definition of 'config_keys'.


==WARNING==


This patch was made only for convenience, and all the parameters passed were not examined for legality. So please use this function carefully and at your own RISK.
