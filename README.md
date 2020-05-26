## About

This is the [php-cs-fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer) configuration file for Laravel applications. The rules used in this configuration are analogues of the [Laravel Preset](https://docs.styleci.io/presets#laravel) rules of StyleCI, extended with a few additional rules of PSR2.

Below are snippets of code for each item, illustrating the appropriate formatting.

## Rules Description

### array_syntax
The same as [short_array_syntax](https://docs.styleci.io/fixers#short_array_syntax) of Laravel Preset.

Input:

```php
$data = array(1, 2, 3);
```

Output:

```php
$data = [1, 2, 3];
```

### binary_operator_spaces
Input:

```php
$a = $b+$c;
```

Output:

```php
$a = $b + $c;
```

### blank_line_after_namespace
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
The same as [psr2_braces](https://docs.styleci.io/fixers#psr2_braces) of Laravel Preset.

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
Input:

```php
(int)$sum;
```

Output:

```php
(int) $sum;
```

### class_attributes_separation
Almost the same as [method_separation](https://docs.styleci.io/fixers#method_separation) of Laravel Preset.

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
Input:

```php
class  Service {}
```

Output:

```php
class Service {}
```
### concat_space
The same as [concat_without_spaces](https://docs.styleci.io/fixers#concat_without_spaces) of Laravel Preset.

Input:

```php
$fullName = $firstName . ' ' . $lastName;
```

Output:

```php
$fullName = $firstName.' '.$lastName;
```

### declare_equal_normalize
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
The same as [post_increment](https://docs.styleci.io/fixers#post_increment) of Laravel Preset.

Input:

```php
++$a;
```

Output:

```php
$a++;
```

### linebreak_after_opening_tag
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
The same as [short_list_syntax](https://docs.styleci.io/fixers#short_list_syntax) of Laravel Preset.

Input:

```php
list($a, $b) = $data;
```

Output:

```php
[$a, $b] = $data;
```

### lowercase_cast
Input:

```php
$a = (DOUBLE) $b;
```

Output:

```php
$a = (double) $b;
```

### lowercase_constants
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
Input:

```php
FOREACH ($items AS $item) {}
```

Output:

```php
foreach ($items as $item) {}
```

### lowercase_static_reference
Input:

```php
STATIC::foo();
```

Output:

```php
static::foo();
```

### magic_constant_casing
Input:

```php
echo __class__;
```

Output:

```php
echo __CLASS__;
```

### magic_method_casing
Input:

```php
parent::__CONSTRUCT($model);
```

Output:

```php
parent::__construct($model);
```

### method_argument_space
Input:

```php
$this->foo($a , $b  ,$c);
```

Output:

```php
$this->foo($a, $b, $c);
```

### multiline_whitespace_before_semicolons (['strategy' => 'no_multi_line'])
The same as [no_multiline_whitespace_before_semicolons](https://docs.styleci.io/fixers#no_multiline_whitespace_before_semicolons) of Laravel Preset.

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
Input:

```php
STRLEN($a);
```

Output:

```php
strlen($a);
```

### no_blank_lines_after_class_opening
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

### no_extra_blank_lines

### no_leading_import_slash

### no_leading_namespace_whitespace

### no_mixed_echo_print

### no_multiline_whitespace_around_double_arrow

### no_short_bool_cast

### no_singleline_whitespace_before_semicolons

### no_spaces_after_function_name

### no_spaces_around_offset

### no_spaces_inside_parenthesis

### no_trailing_comma_in_list_call

### no_trailing_comma_in_singleline_array

### no_trailing_whitespace

### no_trailing_whitespace_in_comment

### no_unneeded_control_parentheses

### no_unused_imports

### no_useless_else

### no_useless_return

### no_whitespace_before_comma_in_array

### no_whitespace_in_blank_line

### normalize_index_brace

### object_operator_without_whitespace

### ordered_imports (['sort_algorithm' => 'alpha'])

### php_unit_fqcn_annotation

### phpdoc_align (['align' => 'left'])

### phpdoc_indent

### phpdoc_inline_tag

### phpdoc_no_access

### phpdoc_no_package

### phpdoc_no_useless_inheritdoc

### phpdoc_order

### phpdoc_scalar

### phpdoc_separation

### phpdoc_single_line_var_spacing

### phpdoc_summary

### phpdoc_to_comment

### phpdoc_trim

### phpdoc_types

### phpdoc_var_without_name

### psr4

### self_accessor

### short_scalar_cast

### simplified_null_return

### single_blank_line_at_eof

### single_blank_line_before_namespace

### single_class_element_per_statement

### single_import_per_statement

### single_line_after_imports

### single_quote

### space_after_semicolon

### standardize_not_equals

### switch_case_semicolon_to_colon

### switch_case_space

### ternary_operator_spaces

### trailing_comma_in_multiline_array

### trim_array_spaces

### unary_operator_spaces

### visibility_required

### whitespace_after_comma_in_array
