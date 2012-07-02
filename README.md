piSlideShow
===========

Jquery based Products Slideshow from all directions

#### Usage

Add jquery, jquery ui and piSlideShow.js to your html source:
  ```html
    <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>
    <script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.8.18/jquery-ui.min.js"></script>
    <script type="text/javascript" src="../lib/js/piSlideshow.js"></script>
  ```
  
Add css to your html source:
  ```css
    <link href="../lib/css/piSlideshow.css" rel="stylesheet" type="text/css" />
  ```

Your HTML may look like this:

  ```html
    <div id="pislideshow" class="slideshow">
      <ul>
	    <li>
	      <div class="main_img"><img src="myimage.jpg" width="100" height="100" /></div>
	      <div class="desc"><p> some descriptions comes here </p></div>
	    </li>
	    <li>
	      <div class="main_img"><img src="myimage.jpg" width="100" height="100" /></div>
	      <div class="desc"><p> some descriptions comes here </p></div>
	    </li>
      </ul>
    </div>
  ```
  `#pislideshow` is the main container.  
  
  Each `li` contains a div with class `.main_img`, this is mandatory. `.main_img` contains your product image which 
  you wish to slide. You may have as many `li`s based on the slides you wants. 
  
  Each `li` also contains description div with class name as `.desc`. This may contain any description you want to show 
  for the product. After the product sliding is over, description will automatically slide down. You must control
  positiion of desc div with your own custom style. To refer to each description div you can use class name as 
  `.slide1 .desc`, where slide1 refers to your first slide. Similarly you can have for all other slides too. 
  
When your Document is ready, call `piSlideShow` on main container of your slides. In this case it is `#pislideshow`
 ```javascript
 
 jQuery(document).ready(function(){
  var options = {
	'slideDirection' : ['right', 'bottom', 'left', 'top']
  }
  $('#pislideshow').pislideshow(options);
});
 ```
### Options Explained

piSlideShow has following options.

* `slideDirection` : **Required** -  Array of Direction (right, bottom, left, top) for each product from where you wish to Slide IN your product. You may specify for each slide or specify just one which will be used for all slide animations.  
                                  -  Eg.: 'slideDirection' : ['right', 'top'] OR 'slideDirection' : ['right']

* `slideTo` : *optional* - Array of positions (numeric) for each product specifying the end slide position of the product.Must be specified for all slides.  
                         - Eg.: 'slideTo' : [-10, 0]  
                         - If nothing is specified, then script will slide-in the product completely inside the main container based on image width.

* `slideFrom` : *optional* - Array of positions (numeric) for each product specifying the start slide position of the product. Must be specified for all slides.  
                           - Eg.: 'slideFrom' : [-500, -200]  
                           - If nothing is specified, then script will move the product completely outside the main container based on image width.

* `animDuration` : *optional* - Array of duration for slide animation for each product. Default value is 1000 (1 sec). You may specify for each slide or specify just one which will be used for all slide animations.
                              - Eg.: 'animDuration' : [1500] OR 'animDuration' : [1500, 500]
 
* `slideDuration` : *optional* - Array of time between two slides. Default value is 5000 (5 secs). You may specify for each slide or specify just one which will be used for all slide animations.  
                               - Eg.: 'slideDuration' : [8000] OR 'slideDuration' : [8000, 5000]
 
* `slideEasing` : *optional* - Array of easing type for each product. Default value is easeOutBack. You may specify for each slide or specify just one which will be used for all slide animations.  
                             - Eg.: 'slideEasing' : ['easeOutBack'] OR 'slideDuration' : ['easeOutBack', 'easeOutElastic']
 
* `preloadImgs` : *optional* - `true` or `false`. Defines if images to be preloaded or not. Default is `true`  
                             - Eg.: 'preloadImgs' : false

* `loader` : **optional** - `true` or `false`. Defines if loaders to be shown or not initally. Default is `true`  
                          - Eg.: 'loader' : false

* `imagesUrl` : **optional** - Relative or Absolute Path to images folder which contains piSlideShow images. Default is `../images/`  
                             - Eg.: 'imagesUrl' : 'http://www.examples.com/frontend/images/' OR 'images' : '../images/slideshow/'

* `anchors` : **optional** - `true` or `false`. Defines if anchor balls to be shown or not. Default is `true`  
                           - Eg.: 'anchors' : false

See demo folder for a sample.