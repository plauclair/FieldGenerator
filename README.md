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

**Versions**

0.9.9 - Fixes an access problem preventing users other than the superadmin to use it and minor bugs

0.9.0 - Adds language fields support.

0.8.0 - Initial release version, with Setup panel support.

**License**

The MIT License (MIT)

Copyright (c) 2014 Pierre-Luc Auclair

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
