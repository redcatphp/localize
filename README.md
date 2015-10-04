 Localize
=========

 Localize is an internationalization toolbox with [Gettext](https://en.wikipedia.org/wiki/Gettext) wrapper, Extractors, Unicode [ CLDR. ](https://en.wikipedia.org/wiki/Common_Locale_Data_Repository)  
 and some internationalization [ ISO ](https://en.wikipedia.org/wiki/International_Organization_for_Standardization) codes.

Gettext wrapper
---------------

 Translator and GettextEmulator are surikat's OOP adapation of [php-gettext](https://launchpad.net/php-gettext/) library.  
 This library provides PHP functions to read MO files even when gettext is not compiled in or when appropriate locale is not present on the system.   
 The structure of locales is $projectHome/langs/$lang/LC\_MESSAGES/messages.mo, eg: www/langs/fr/LC\_MESSAGES/messages.mo. It support cache regeneration without restart apache by dint of use a copy of MO file named with timestamp suffix. To enable look for last message.$time.mo set dev to true. You'll have to create this file manualy or with other i18n tool. 
```php
Translator::getInstance()->dev = true;  
            
```
   
 You can include "\_\_.php" to use procedural function based on *Wild\\Localize\\Translator* static current instance. 
```php
echo \_\_($msgid);  
echo n\_\_($singular,$plural,$number);  
            
```


CLDR - Punic
------------

 Punic - PHP translation and localization made easy. It contain internationalization data for language, calendar, territory, number, unit, phone, currency, plural and misc. Punic is a third party [ CLDR. ](https://en.wikipedia.org/wiki/Common_Locale_Data_Repository) library. See the official [Punic documentation](http://punic.github.io/).
