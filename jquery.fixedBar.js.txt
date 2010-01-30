/*
 * Fixed Bar -  Places a bar non-moving div on the top or bottom of the webpage
 * By Tom LeZotte (http://plugins.jquery.com/project/fixed-bar)
 * Copyright (c) 2009 Tom LeZotte (tlezotte@gmail.com)
 * Licensed under the MIT License: http://www.opensource.org/licenses/mit-license.php
*/


(function($){  

	$.fn.fixedBar = function(options) {  
		//Set Defaults
		var defaults = {
			position: 'bottom',
			height: 25,
			style: 'ui-widget-content'
		};
		$.extend(defaults, options);  	//Merge "defaults" and "options"

		var selector = (this.selector=='') ? '#fixedBar' : this.selector;		//Set selector id
		var height = defaults.height*2+20;
		console.log(height);
		
		//Set CSS styles
		 var cssObj = {
			'position' : 'fixed',
			'left' : '0',
			'width' : '100%',
			'padding' : '5px',
			'height' : defaults.height
		}
		var positionObj = (defaults.position=='bottom') ? {'bottom':'0'} : {'top':'0'};		//Set CSS position style
		$.extend(cssObj, positionObj);		//Merge style items

		/* ===== Set ===== */
		$('body').css("padding-" + defaults.position,height);		//Add fixed bar padding to page
		$(selector).addClass(defaults.style).css(cssObj); 			//Apply Theme class and CSS style to bar
	}

})(jQuery); 