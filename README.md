Иницилизация в scss

.fullpage-wrapper {
	width: 100%!important;
	transform: none!important;
	
	.fp-section {
		&.active {
			visibility: visible;
			opacity: 1;
			z-index: 1;
		}
		
		width: 100%!important;
		position: absolute;
		left: 0;
		top: 0;
		visibility: hidden;
		opacity: 0;
		z-index: 0;
		transition: all .7s ease-in-out;
		
		.fp-slidesContainer {
			width: 100%!important;
			transform: none!important;
			
			.fp-slide {
				&.active {
					visibility: visible;
					opacity: 1;
					z-index: 1;
				}
				
				width: 100%!important;
				position: absolute;
				left: 0;
				top: 0;
				visibility: hidden;
				opacity: 0;
				z-index: 0;
				transition: all .7s ease-in-out;
			}
		}
	}
}

js:

	new fullpage('#fullpage', {
		//options here
		css3: true,
		controlArrows: false,
		anchors: ['home', 'girl', 'services', 'contact'],
		menu: '#sideMenu',
		loopBottom: true,
		parallax: true,
		scrollHorizontally:true,
		fadingEffect:true,
		scrollingSpeed: 1000
	});
	//methods
	fullpage_api.setAllowScrolling(true);
