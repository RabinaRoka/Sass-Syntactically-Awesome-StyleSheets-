One feature of Sass that's different than CSS is it uses variables. They are declared and set to store data, similar to JavaScript.

In JavaScript, variables are defined using the let and const keywords. In Sass, variables start with a $ followed by the variable name.


#In Sass, a mixin is a group of CSS declarations that can be reused throughout the style sheet. The definition starts with the @mixin at-rule, followed by a custom name. You apply the mixin using the @include at-rule


#The @if directive in Sass is useful to test for a specific case - it works just like the if statement in JavaScript.

@mixin make-bold($bool) {
  @if $bool == true {
    font-weight: bold;
  }
}
And just like in JavaScript, the @else if and @else directives test for more conditions:



##The @while directive is an option with similar functionality to the JavaScript while loop. It creates CSS rules until a condition is met.

The @for challenge gave an example to create a simple grid system. This can also work with @while.

#Partials in Sass are separate files that hold segments of CSS code. These are imported and used in other Sass files. This is a great way to group similar code into a module to keep it organized.


#Names for partials start with the underscore (_) character, which tells Sass it is a small segment of CSS and not to convert it into a CSS file. Also, Sass files end with the .scss file extension. To bring the code in the partial into another Sass file, use the @import directive.

For example, if all your mixins are saved in a partial named "_mixins.scss", and they are needed in the "main.scss" file, this is how to use them in the main file:

@import 'mixins'
