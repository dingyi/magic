magic
=====

CSS3 Animations with special effects. Now on beta, more effects coming soon. Many thanks to [daneden](http://daneden.me/animate/) for inspiration!
My next step is to minifing the code.
Take a look at the demo [link to demo page](http://www.minimamente.com/magic-css3-animations)

I fork this project and made them for SASS.

In fact, almost every websites you don't need all animations at all, so you just need to import the ones you wanna use.


##Installation


This fork need Bourbon's keyframe minxin, include it first, and then include this project.
and
import them in your sass/scss file. eg: import 'magic/swap'

##Usage

This is a sample code on hover with jQuery, first you include the class "magictime" and after your desired animation.
```js
$('.yourdiv').hover(function () {
  $(this).addClass('magictime puffIn');
});
```

If you want to load the animation after certain time, you can use this example:
```js
//set timer to 5 seconds, after that, load the magic animation
setTimeout(function(){
  	$('.yourdiv').addClass('magictime puffIn');
}, 5000);
```

You can change the time of the animation by set the class "magictime" for example:
```css
.magictime {
    @include animation-duration(3s);
}
```

Default CSS timing is:
```css
.magictime {
    @include animation-duration(1s);
}
```

If you want to assign the timing to a specific animation, you can use that code (use 2 class):
```css
.magictime.magic {
    @include animation-duration(10s);
}
```
