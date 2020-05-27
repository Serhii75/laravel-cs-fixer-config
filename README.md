## About

This is the [php-cs-fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer) configuration file for Laravel applications. The rules used in this configuration are analogues of the [Laravel Preset](https://docs.styleci.io/presets#laravel) rules of StyleCI, extended with a few additional rules of PSR2.

## How to use

> This repo contains configuration file only, and you should have [FriendsOfPHP/PHP-CS-Fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer) installed.

Copy `.php_cs.dist` file of this repo into the root directory of your project. then use the commands as described in the php-cs-fixer documentation.

## Rules Description

Below you can find snippets of code for each item, illustrating the appropriate formatting.

### array_syntax
PHP arrays should be declared using the configured syntax.

> The same as [short_array_syntax](https://docs.styleci.io/fixers#short_array_syntax) of Laravel Preset.

Input:

```php
$data = array(1, 2, 3);
```

Output:

```php
$data = [1, 2, 3];
```

### binary_operator_spaces
Binary operators should be surrounded by space as configured.

Input:

```php
$a = $b+$c;
```

Output:

```php
$a = $b + $c;
```

### blank_line_after_namespace
There MUST be one blank line after the namespace declaration.

Input:

```php
namespace App;
use Cache;
```

Output:

```php
namespace App;

use Cache;
```

### blank_line_after_opening_tag
Ensure there is no code on the same line as the PHP open tag and it is followed by a blank line.

Input:

```php
<?php
namespace App;
```

Output:

```php
<?php

namespace App;
```

### blank_line_before_return
An empty line feed should precede a return statement.

Input:

```php
$products = Product::get();
return $products;
```

Output:

```php
$products = Product::get();

return $products;
```

### braces
The body of each structure MUST be enclosed by braces. Braces should be properly placed. Body of braces should be properly indented.

> The same as [psr2_braces](https://docs.styleci.io/fixers#psr2_braces) of Laravel Preset.

Input:

```php
if ($a === $b) return 'The same';
```

Output:

```php
if ($a === $b) {
    return 'The same';
}
```

### cast_spaces
A single space MUST be between cast and variable.

Input:

```php
(int)$sum;
```

Output:

```php
(int) $sum;
```

### class_attributes_separation
Class, trait and interface elements must be separated with one blank line.

> Almost the same as [method_separation](https://docs.styleci.io/fixers#method_separation) of Laravel Preset.

Input:

```php
class Foo
{
    private $a;
    private $b;

    public function bar()
    {
    }
    public function baz()
    {
    }
}
```

Output:

```php
class Foo
{
    private $a;

    private $b;

    public function bar()
    {
    }

    public function baz()
    {
    }
}
```


### class_definition
Whitespace around the keywords of a class, trait or interfaces definition should be one space.

Input:

```php
class  Service {}
```

Output:

```php
class Service {}
```
### concat_space
Concatenation should be used without spaces.
> The same as [concat_without_spaces](https://docs.styleci.io/fixers#concat_without_spaces) of Laravel Preset.

Input:

```php
$fullName = $firstName . ' ' . $lastName;
```

Output:

```php
$fullName = $firstName.' '.$lastName;
```

### declare_equal_normalize
Equal sign in declare statement MUST NOT be surrounded by spaces.

Input:

```php
declare($tick = 1);
```

Output:

```php
declare($tick=1);
```
### elseif
Input:

```php
if ($a) {
    //
} else if ($b) {
    //
}
```

Output:

```php
if ($a) {
    //
} elseif ($b) {
    //
}
```

### encoding
PHP code MUST use only UTF-8 without BOM (remove BOM).

### full_opening_tag
PHP code must use the long `<?php` tags or short-echo `<?=` tags and not other tag variations.

Input:

```php
<?

namespace App;
```

Output:

```php
<?php

namespace App;
```

### function_declaration
Spaces should be properly placed in a function declaration.

Input:

```php
public function  foo ( $bar , $baz  )
{
    return 'Bad';
}
```

Output:

```php
public function foo($bar, $baz)
{
    return 'Good';
}
```

### function_typehint_space
Ensure single space between function's argument and its typehint.

Input:

```php
public function foo(string  $bar)
{
    return 'Bad';
}
```

Output:

```php
public function foo(string $bar)
{
    return 'Good';
}
```
### heredoc_to_nowdoc
Convert `heredoc`to `nowdoc` where possible.

Input:

```php
$a = <<<"TEST"
Foo
TEST;
```

Output:

```php
$a = <<<'TEST'
Foo
TEST;
```

### include
Include/Require and file path should be divided with a single space. File path should not be placed under brackets.

Input:

```php
include      'first.php';
include_once('second.php');
```

Output:

```php
include 'first.php';
include_once 'second.php';
```

### increment_style (['style' => 'post'])
Post incrementation/decrementation should be used if possible.
> The same as [post_increment](https://docs.styleci.io/fixers#post_increment) of Laravel Preset.

Input:

```php
++$a;
```

Output:

```php
$a++;
```

### linebreak_after_opening_tag
Ensure there is no code on the same line as the PHP open tag.

Input:

```php
<?php $a = 1;
```

Output:

```php
<?php
$a = 1;
```

### list_syntax (['syntax' => 'short'])
Destructuring assignment should use the short syntax.
> The same as [short_list_syntax](https://docs.styleci.io/fixers#short_list_syntax) of Laravel Preset.

Input:

```php
list($a, $b) = $data;
```

Output:

```php
[$a, $b] = $data;
```

### lowercase_cast
Cast should be written in lower case.

Input:

```php
$a = (DOUBLE) $b;
```

Output:

```php
$a = (double) $b;
```

### lowercase_constants
The PHP constants `true`, `false`, and `null` MUST be in lower case.

Input:

```php
$a = TRUE;
$b = NULL;
```

Output:

```php
$a = true;
$b = null;
```

### lowercase_keywords
PHP keywords MUST be in lower case.

Input:

```php
FOREACH ($items AS $item) {}
```

Output:

```php
foreach ($items as $item) {}
```

### lowercase_static_reference
Class static references `self`, `static` and `parent` MUST be in lower case.

Input:

```php
STATIC::foo();
```

Output:

```php
static::foo();
```

### magic_constant_casing
Magic constants should be referred to using the correct casing.

Input:

```php
echo __class__;
```

Output:

```php
echo __CLASS__;
```

### magic_method_casing
Magic method definitions and calls must be using the correct casing.

Input:

```php
parent::__CONSTRUCT($model);
```

Output:

```php
parent::__construct($model);
```

### method_argument_space
In arguments and calls, there MUST be 0 spaces before and 1 space after each comma.

Input:

```php
$this->foo($a , $b  ,$c);
```

Output:

```php
$this->foo($a, $b, $c);
```

### multiline_whitespace_before_semicolons (['strategy' => 'no_multi_line'])
There MUST NOT be a newline before a semicolon.
> The same as [no_multiline_whitespace_before_semicolons](https://docs.styleci.io/fixers#no_multiline_whitespace_before_semicolons) of Laravel Preset.

Input:

```php
$this->foo()
    ->bar()
    ;
```

Output:

```php
$this->foo()
    ->bar();
```

### native_function_casing
Function defined by PHP should be called using the correct casing.

Input:

```php
STRLEN($a);
```

Output:

```php
strlen($a);
```

### no_blank_lines_after_class_opening
There should be no empty lines after class opening brace.

Input:

```php
class Foo
{
    

    public function bar()
    {
    }
}
```

Output:

```php
class Foo
{
    public function bar()
    {
    }
}
```

### no_blank_lines_after_phpdoc
There should not be blank lines between docblock and the documented element.

Input:

```php
/**
 * Bar method description.
 */

public function bar()
{
}
```

Output:

```php
/**
 * Bar method description.
 */
public function bar()
{
}
```

### no_closing_tag
The closing `?>` tag MUST be omitted from files containing only PHP.

Input:

```php
<?php

class Foo
{
}
?>
```

Output:

```php
<?php

class Foo
{
}
```

### no_empty_phpdoc
There should not be empty PHPDoc blocks.

Input:

```php
/**
 *
 */
public function bar()
{
}
```

Output:

```php
public function bar()
{
}
```

### no_empty_statement
Remove useless semicolon statements.

Input:

```php
$a = 1;;
```

Output:

```php
$a = 1;
```

### no_extra_blank_lines
Removes extra blank lines and/or blank lines following configuration.

Input:

```php
public function foo()
{
}


public function bar()
{
}
```

Output:

```php
public function foo()
{
}

public function bar()
{
}
```

### no_leading_import_slash
Remove leading slashes in `use` clauses.

Input:

```php
use \Foo;
```

Output:

```php
use Foo;
```

### no_leading_namespace_whitespace
The namespace declaration line shouldn't contain leading whitespace.

Input:

```php
  namespace Foo;
```

Output:

```php
namespace Foo;
```

### no_mixed_echo_print
Converts print language construct to echo if possible.
> The same as [print_to_echo](https://docs.styleci.io/fixers#print_to_echo) of Laravel Preset.

Input:

```php
print 'Hello World';
```

Output:

```php
echo 'Hello World';
```

### no_multiline_whitespace_around_double_arrow
Operator `=>` should not be surrounded by multi-line whitespaces.

Input:

```php
$a = [ 'foo'

 => 'bar'
];
```

Output:

```php
$a = ['foo' => 'bar'];
```

### no_short_bool_cast
Short cast bool using double exclamation mark should not be used.

Input:

```php
$a = !!$b;
```

Output:

```php
$a = (bool) $b;
```

### no_singleline_whitespace_before_semicolons
Single-line whitespace before closing semicolon are prohibited.

Input:

```php
foo() ;
```

Output:

```php
foo();
```

### no_spaces_after_function_name
When making a method or function call, there MUST NOT be a space between the method or function name and the opening parenthesis.

Input:

```php
foo ();
```

Output:

```php
foo();
```

### no_spaces_around_offset
There MUST NOT be spaces around offset braces.
> The same as [no_spaces_inside_offset](https://docs.styleci.io/fixers#no_spaces_inside_offset) and [no_spaces_outside_offset](https://docs.styleci.io/fixers#no_spaces_outside_offset) of Laravel Preset.

Input:

```php
$data [ 'a' ];
```

Output:

```php
$data['a'];
```

### no_spaces_inside_parenthesis
There MUST NOT be a space after the opening parenthesis. There MUST NOT be a space before the closing parenthesis.

Input:

```php
if ( $a ) {
    //
};
```

Output:

```php
if ($a) {
    //
};
```

### no_trailing_comma_in_list_call
Remove trailing commas in list function calls. 

Input:

```php
list($a, $b) = foo();
```

Output:

```php
list($a, $b,) = foo();
```

### no_trailing_comma_in_singleline_array
PHP single-line arrays should not have trailing comma.

Input:

```php
$data = ['a', 'b',];
```

Output:

```php
$data = ['a', 'b'];
```

### no_trailing_whitespace
Remove trailing whitespace at the end of non-blank lines.

Input:

```php
$a = 1;   
```

Output:

```php
$a = 1;
```

### no_trailing_whitespace_in_comment
There MUST be no trailing spaces inside comment or PHPDoc.

### no_unneeded_control_parentheses
Removes unneeded parentheses around control statements.

Input:

```php
break (2);
```

Output:

```php
break 2;
```

### no_unused_imports
Unused `use` statements must be removed.

Input:

```php
use App\Post;
use App\User;

$user = new User;
```

Output:

```php
use App\User;

$user = new User;
```

### no_useless_else
There should not be useless `else` cases.

Input:

```php
if ($a) {
    return true;
} else {
    return false;
}
```

Output:

```php
if ($a) {
    return true;
}
  
return false;
```

### no_useless_return
There should not be an empty `return` statement at the end of a function.

Input:

```php
if ($a) {
    return;
}

return;
```

Output:

```php
if ($a) {
    return;
}
```

### no_whitespace_before_comma_in_array
In array declaration, there MUST NOT be a whitespace before each comma.

Input:

```php
[1 , 2  , 3];
```

Output:

```php
[1, 2, 3];
```

### no_whitespace_in_blank_line
Remove trailing whitespace at the end of blank lines. 

### normalize_index_brace
Remove trailing whitespace at the end of blank lines.

### object_operator_without_whitespace
There should not be space before or after object `T_OBJECT_OPERATOR ->`.

Input:

```php
$foo -> bar;
```

Output:

```php
$foo->bar;
```

### ordered_imports (['sort_algorithm' => 'alpha'])
Order import statements alphabetically.
> The same as [alpha_ordered_imports](https://docs.styleci.io/fixers#alpha_ordered_imports) of Laravel Preset.

Input:

```php
use Illuminate\Support\Str;
use App\Services\ProductService;
```

Output:

```php
use App\Services\ProductService;
use Illuminate\Support\Str;
```

### phpdoc_align (['align' => 'left'])
Align all multiline comments to match their first line.
>Almost the same as [align_phpdoc](https://docs.styleci.io/fixers#align_phpdoc) of Laravel Preset. The difference is phpdoc_align uses 1 space instead of 2 as in align_phpdoc.

Input:

```php
/**
 * Create a notification instance.
 *
 * @param  string       $token
 * @param string   $path
 */
```

Output:

```php
/**
 * Create a notification instance.
 *
 * @param string $token
 * @param string $path
 */
```

### phpdoc_indent
Docblocks should have the same indentation as the documented subject.

Input:

```php
/**
 * The table associated with the model.
 *
 * @var string
 */
    protected $table;
```

Output:

```php
    /**
     * The table associated with the model.
     *
     * @var string
     */
    protected $table;
```

### phpdoc_inline_tag
Fix PHPDoc inline tags, make `@inheritdoc` always inline.

Input:

```php
/**
 * @inheritDocs
 */
```

Output:

```php
/**
 * {@inheritdoc}
 */
```

### phpdoc_no_access
`@access` annotations should be omitted from PHPDoc.
Input:

```php
/**
 * @var string
 * @access protected
 */
protected $table;
```

Output:

```php
/**
 * @var string
 */
protected $table;
```

### phpdoc_no_package
`@package` and `@subpackage` annotations should be omitted from PHPDoc.
Input:

```php
/**
 * Class Product.
 *
 * @package Product
 */
class Product {}
```

Output:

```php
/**
 * Class Product.
 */
class Product {}
```

### phpdoc_order
Annotations in PHPDoc should be ordered so that `@param` annotations come first, then `@throws` annotations, then `@return` annotations.
> There is no such rule in Laravel preset of StyleCI, but you can find it in [Recommended](https://docs.styleci.io/presets#recommended).

Input:

```php
/**
 * @return Experience
 *
 * @throws Exception
 *
 * @param Request $request
 * @param User $user
 */
```

Output:

```php
/**
 * @param Request $request
 * @param User $user
 *
 * @throws Exception
 *
 * @return Experience
 */
```

### phpdoc_scalar
Scalar types should always be written in the same form. `int` not `integer`, `bool` not `boolean`, `float` not `real` or `double`.
Input:

```php
/**
 * @param integer $a
 * @param boolean $b
 *
 * @return double
 */
```

Output:

```php
/**
 * @param int $a
 * @param bool $b
 *
 * @return float
 */
```

### phpdoc_separation
Annotations in PHPDoc should be grouped together so that annotations of the same type immediately follow each other, and annotations of a different type are separated by a single blank line.
> This rule also belongs to [Recommended](https://docs.styleci.io/presets#recommended) preset.

Input:

```php
/**
 * Update the post.
 * @param Post $post
 * @param Request $request
 * @throws Exception
 * @return Post
 */
```

Output:

```php
/**
 * Update the post.
 *
 * @param Post $post
 * @param Request $request
 *
 * @throws Exception
 *
 * @return Post
 */
```

### phpdoc_single_line_var_spacing
Single line `@var` PHPDoc should have proper spacing.
Input:

```php
/**@var   User   $user   */
```

Output:

```php
/**@var User $user */
```

### phpdoc_summary
PHPDoc summary should end in either a full stop, exclamation mark, or question mark.

Input:

```php
/**
 * Register media collection
 */
```

Output:

```php
/**
 * Register media collection.
 */
```

### phpdoc_trim
PHPDoc should start and end with content, excluding the very first and last line of the docblocks.

Input:

```php
/**
 *
 * Register media collection.
 *
 */
```

Output:

```php
/**
 * Register media collection.
 */
```

### phpdoc_types
The correct case must be used for standard PHP types in PHPDoc.

Input:

```php
/**
 * @param INT $count
 */
```

Output:

```php
/**
 * @param int $count
 */
```

### phpdoc_var_without_name
`@var` and `@type` annotations of classy properties should not contain the name.

Input:

```php
/**
 * @var string $table
 */
protected $table;
```

Output:

```php
/**
 * @var string
 */
protected $table;
```

### psr4
Class names should match the file name.

> Risky rule: this fixer may change your class name, which will break the code that depends on the old name.

### self_accessor
Inside class or interface element self should be preferred to the class name itself.

Input:

```php
class Foo
{
    public const BAR = 'bar';

    public function getBar()
    {
        return Foo::BAR;
    }
}
```

Output:

```php
class Foo
{
    public const BAR = 'bar';

    public function getBar()
    {
        return self::BAR;
    }
}
```

### short_scalar_cast
Cast `(boolean)` and `(integer)` should be written as `(bool)` and `(int)`, `(double)` and `(real)` as `(float)`, `(binary)` as `(string)`.

Input:

```php
$a = (integer) $b;
```

Output:

```php
$a = (int) $b;
```

### simplified_null_return
A return statement wishing to return `void` should not return `null`.

Input:

```php
public function foo(): void
{
    return null;
}
```

Output:

```php
public function foo(): void
{
    return;
}
```

### single_blank_line_at_eof
A PHP file without end tag must always end with a single empty line feed.

### single_blank_line_before_namespace
There should be exactly one blank line before a namespace declaration.

Input:

```php
<?php


namespace App;
```

Output:

```php
<?php

namespace App;
```

### single_class_element_per_statement
There MUST NOT be more than one property or constant declared per statement.

Input:

```php
class Foo
{
    public const BAR = 'bar', BAZ = 'baz';
}
```

Output:

```php
class Foo
{
    public const BAR = 'bar';

    public const BAZ = 'baz';
}
```

### single_import_per_statement
There MUST be one use keyword per declaration.

Input:

```php
use Foo, Bar;
```

Output:

```php
use Foo;
use Bar;
```

### single_line_after_imports
Each namespace use MUST go on its own line and there MUST be one blank line after the use statements block.

Input:

```php
<?php namespace App;


use Bar;
use Baz;


class Foo
{
}
```

Output:

```php
<?php 

namespace App;

use Bar;
use Baz;

class Foo
{
}
```

### single_quote
Convert double quotes to single quotes for simple strings.

Input:

```php
$text = "Hello World";
```

Output:

```php
$text = 'Hello World';
```

### space_after_semicolon
Fix whitespace after a semicolon.

### standardize_not_equals
Replace all `<>` with `!=`.

Input:

```php
$a = $b <> $c;
```

Output:

```php
$a = $b != $c;
```

### switch_case_semicolon_to_colon
A case should be followed by a colon and not a semicolon.

Input:

```php
switch ($type) {
    case 'foo';
        break;
}
```

Output:

```php
switch ($type) {
    case 'foo':
        break;
}
```

### switch_case_space
Removes extra spaces between colon and case value.

Input:

```php
switch ($type) {
    case 'foo'  :
        break;
}
```

Output:

```php
switch ($type) {
    case 'foo':
        break;
}
```

### ternary_operator_spaces
Standardize spaces around ternary operator.

Input:

```php
$result = $foo->bar?   true:  false;
```

Output:

```php
$result = $foo->bar ? true : false;
```

### trailing_comma_in_multiline_array
PHP multi-line arrays should have a trailing comma.

Input:

```php
$data = [
    'a' => 1,
    'b' => 2
];
```

Output:

```php
$data = [
    'a' => 1,
    'b' => 2,
];
```

### trim_array_spaces
Arrays should be formatted like function/method arguments, without leading or trailing single line space.

```php
$data = [ 1,   2,  3 ];
```

Output:

```php
$data = [1, 2, 3];
```

### unary_operator_spaces
Unary operators should be placed adjacent to their operands.

```php
$counter ++;
```

Output:

```php
$counter++;
```

### visibility_required
Visibility MUST be declared on all properties and methods; `abstract` and `final` MUST be declared before the visibility; `static` MUST be declared after the visibility.

```php
static protected $foo;
```

Output:

```php
protected static $foo;
```

### whitespace_after_comma_in_array
In array declaration, there MUST be a whitespace after each comma.

```php
$data = [1,2,3];
```

Output:

```php
$data = [1, 2, 3];
```
