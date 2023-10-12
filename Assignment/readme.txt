
Variables-> Variables are a way to store information so that I could re-use later.
I used _config.scss to store variable 
{
$font-stack: Arial, Helvetica, sans-serif;
$light-color: #e5e5e7;
$primary-color: #C1DBB3;
$secondary-color: #BBD8AC;
$color-recent:#486F34;
$image: "img";
$rgbheader:#85C190;
}

Custom Properties-> 
Interpolation->Interpolation returns unquoted strings that can't be used for any further and is basically an insertion. 
#{$image}

Nesting->Sass has a feature that lets me nest css selectors similar to that of the html. i have used to nest nav and ul tags in home.scss

.container {
	display: grid;
	@include set-background($primary-color);
    row-gap: 20px;
nav{
	ul{
	........
		}
	}

	}


Placeholder Selectors-> it is used to write custum sass library similar to the one i used in _button.scss to define the method for highilighting the button and is also used its similar to class selector but will not be included in the css output
%btn{
    ........
    }



Mixins-> The @mixin directive lets you create CSS code that is to be reused throughout the code

@mixin set-background($color) {
}

@include -> The @include directive is created to let you use (include) the mixin.
	@include set-background($primary-color);


Functions-> Functions are defined using the @function at-rule, which is written @function it will also contain return statement
@function set-text-color($color) {
    @if(lightness($color) > 70) {
        @return #000;
    }
    @else {
        @return #fff;
    }
}



&-child class name:  Sass that’s used in nested selectors to refer to the outer selector
@extend in button.scss
Place holder selector ia also used its similar to class selector but will not be included in the css output

