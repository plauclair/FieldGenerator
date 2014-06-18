# Field Generator module documentation
Field Generator is a ProcessWire module to help you create random character strings and automatically assign them to one or multiple fields of your choice when a page is created.
When setup, it will automatically do so whether you create a page through the administration panel or through code, meaning you don’t need to set $page-\>name or any other field of your choice, it just works automagically.
Field Generator uses PHP’s openssl\_random\_pseudo\_bytes() function to generate its random strings. It thus has both PHP \>= 5.3.0 and OpenSSL as dependencies.
## Usage
After installation, add rules through Setup \> Field Generator. That’s it! Rules **only** run when first creating the page.
## Rule settings
**Parent ID** specifies which immediate page parent the rule will be applied on.
**Template** specifies what template the rule applies on.
You can mix both _Parent ID_ and _Template_ to use them as a combination. Rules will apply only if the two conditions are met.
**Field** specifies what field will be generated.
**Length** sets the generated string length.
**Dictionary** contains the characters the rule can use. It can be any character, but make sure the specified field supports them.
## About rule conflicts
Field Generator makes no effort to find conflicting rules. If two different rules happen to apply on any given field, both will run. We trust you on that one.