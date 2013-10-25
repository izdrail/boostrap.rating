Bootstrap Rating Input in 2Kb

This is another plugin that eases the generation of rating stars for jQuery and Bootstrap.

It generates widgets like this:

Rating example

But, why another damn rating plugin???

After searching for existing widgets, I found three categories of them:

The ones that depends on PNG images.
The ones that adds A LOT of JavaScript and CSS code to my project.
The ones that adds A LOT of JavaScript and CSS code and depends on PNG images.
I don't want to add a whole multipurpose library just to put a few stars in my interface, I want my rating stars to look awesome in retina screens without worrying about image versions and dynamically replacing them, and Bootstrap already includes a set of beautifully designed vectorial icons by Glyphicons, so I thought I could create something simpler.

Ok, enough talking, tell me how this thing works!

Download bootstrap-rating-input.min.js and put it wherever you usually put JavaScripts in your project. Include it on pages where you want to have forms with ratings:

<script src="path/to/javascripts/bootstrap-rating-input.min.js" type="text/javascript"></script>
Now add a input of type number to your forms and add the class rating to it:
<input class="rating" data-max="4" data-min="0" id="some_id" name="your_awesome_parameter" type="number" />

<input type="number" name="your_awesome_parameter" id="some_id" class="rating" />
That's all! When page loads, you'll find a few stars where you'd expect to find the input. It works just like most of rating plugins, but you don't need to learn anything about options or initializations, it just works out of the box.

Wait, where has my input gone?
$('input.my_class').rating();

The plugin replaces your number input by a hidden field with identical name and id and adds interactive stars that will catch your clicks and save the selected values into the hidden field. In this way the form can be submitted or value readed by jQuery normally.

Nice, but I want to use a different number of stars

Sure! You can set min and max values adding data-min and data-max:


And what about clearing the stars?

Requirements

You know... Twitter Bootstrap and jQuery!

Can I generate read-only stars for displaying?

If you think about it you don't want to use a plugin to generate static HTML code that is as simple as this:


This plugin is bassed on this guy version

https://github.com/javiertoledo/bootstrap-rating-input

