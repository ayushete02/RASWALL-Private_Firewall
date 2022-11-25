 var \_\_ez=\_\_ez||{};\_\_ez.stms=Date.now();\_\_ez.evt={};\_\_ez.script={};\_\_ez.ck=\_\_ez.ck||{};\_\_ez.template={};\_\_ez.template.isOrig=true;\_\_ez.queue=function(){var e=0,i=0,t=\[\],n=!1,s=\[\],r=\[\],o=!0,a=function(e,i,n,s,r,o,a){var l=this;this.name=e,this.funcName=i,this.parameters=null===n?null:n instanceof Array?n:\[n\],this.isBlock=s,this.blockedBy=r,this.deleteWhenComplete=o,this.isError=!1,this.isComplete=!1,this.isInitialized=!1,this.proceedIfError=a,this.isTimeDelay=!1,this.process=function(){u("... func = "+e),l.isInitialized=!0,l.isComplete=!0,u("... func.apply: "+e);var i=l.funcName.split("."),n=null;i.length>3||(n=3===i.length?window\[i\[0\]\]\[i\[1\]\]\[i\[2\]\]:2===i.length?window\[i\[0\]\]\[i\[1\]\]:window\[l.funcName\]),null!=n&&n.apply(null,this.parameters),!0===l.deleteWhenComplete&&delete t\[e\],!0===l.isBlock&&(u("----- F'D: "+l.name),f())}},l=function(e,i,t,n,s,r,o){var a=this;this.name=e,this.path=i,this.async=s,this.defer=r,this.isBlock=t,this.blockedBy=n,this.isInitialized=!1,this.isError=!1,this.isComplete=!1,this.proceedIfError=o,this.isTimeDelay=!1,this.isPath=function(e){return"/"===e\[0\]&&"/"!==e\[1\]},this.getSrc=function(e){return void 0!==window.\_\_ezScriptHost&&this.isPath(e)?window.\_\_ezScriptHost+e:e},this.process=function(){a.isInitialized=!0,u("... file = "+e);var i=document.createElement("script");i.src=this.getSrc(this.path),!0===s?i.async=!0:!0===r&&(i.defer=!0),i.onerror=function(){u("----- ERR'D: "+a.name),a.isError=!0,!0===a.isBlock&&f()},i.onreadystatechange=i.onload=function(){var e=i.readyState;u("----- F'D: "+a.name),e&&!/loaded|complete/.test(e)||(a.isComplete=!0,!0===a.isBlock&&f())},document.getElementsByTagName("head")\[0\].appendChild(i)}},c=function(e,i){this.name=e,this.path="",this.async=!1,this.defer=!1,this.isBlock=!1,this.blockedBy=\[\],this.isInitialized=!0,this.isError=!1,this.isComplete=i,this.proceedIfError=!1,this.isTimeDelay=!1,this.process=function(){}};function d(e){!0!==h(e)&&0!=o&&e.process()}function h(e){if(!0===e.isTimeDelay&&!1===n)return u(e.name+" blocked = TIME DELAY!"),!0;if(e.blockedBy instanceof Array)for(var i=0;i<e.blockedBy.length;i++){var s=e.blockedBy\[i\];if(!1===t.hasOwnProperty(s))return u(e.name+" blocked = "+s),!0;if(!0===e.proceedIfError&&!0===t\[s\].isError)return!1;if(!1===t\[s\].isComplete)return u(e.name+" blocked = "+s),!0}return!1}function u(e){var i=window.location.href,t=new RegExp("\[?&\]ezq=(\[^&#\]\*)","i").exec(i);"1"===(t?t\[1\]:null)&&console.debug(e)}function f(){++e>200||(u("let's go"),m(s),m(r))}function m(e){for(var i in e)if(!1!==e.hasOwnProperty(i)){var t=e\[i\];!0===t.isComplete||h(t)||!0===t.isInitialized||!0===t.isError?!0===t.isError?u(t.name+": error"):!0===t.isComplete?u(t.name+": complete already"):!0===t.isInitialized&&u(t.name+": initialized already"):t.process()}}return window.addEventListener("load",(function(){setTimeout((function(){n=!0,u("TDELAY -----"),f()}),5e3)}),!1),{addFile:function(e,i,n,o,a,c,h,u){var f=new l(e,i,n,o,a,c,h);!0===u?s\[e\]=f:r\[e\]=f,t\[e\]=f,d(f)},addDelayFile:function(e,i){var n=new l(e,i,!1,\[\],!1,!1,!0);n.isTimeDelay=!0,u(e+" ... FILE! TDELAY"),r\[e\]=n,t\[e\]=n,d(n)},addFunc:function(e,n,o,l,c,h,u,f,m){!0===h&&(e=e+"\_"+i++);var p=new a(e,n,o,l,c,u,f);!0===m?s\[e\]=p:r\[e\]=p,t\[e\]=p,d(p)},addDelayFunc:function(e,i,n){var s=new a(e,i,n,!1,\[\],!0,!0);s.isTimeDelay=!0,u(e+" ... FUNCTION! TDELAY"),r\[e\]=s,t\[e\]=s,d(s)},items:t,processAll:f,setallowLoad:function(e){o=e},markLoaded:function(e){if(e&&0!==e.length){if(e in t){var i=t\[e\];!0===i.isComplete?u(i.name+" "+e+": error loaded duplicate"):(i.isComplete=!0,i.isInitialized=!0)}else t\[e\]=new c(e,!0);u("markLoaded dummyfile: "+t\[e\].name)}},logWhatsBlocked:function(){for(var e in t)!1!==t.hasOwnProperty(e)&&h(t\[e\])}}}();\_\_ez.evt.add=function(e,t,n){e.addEventListener?e.addEventListener(t,n,!1):e.attachEvent?e.attachEvent("on"+t,n):e\["on"+t\]=n()},\_\_ez.evt.remove=function(e,t,n){e.removeEventListener?e.removeEventListener(t,n,!1):e.detachEvent?e.detachEvent("on"+t,n):delete e\["on"+t\]};\_\_ez.script.add=function(e){var t=document.createElement("script");t.src=e,t.async=!0,t.type="text/javascript",document.getElementsByTagName("head")\[0\].appendChild(t)};\_\_ez.dot={};\_\_ez.queue.addFile('/detroitchicago/boise.js', '/detroitchicago/boise.js?gcb=195-18&cb=2', true, \[\], true, false, true, false);\_\_ez.queue.addFile('/detroitchicago/memphis.js', '/detroitchicago/memphis.js?gcb=195-18&cb=21', true, \[\], true, false, true, false);\_\_ez.queue.addFile('/detroitchicago/minneapolis.js', '/detroitchicago/minneapolis.js?gcb=195-18&cb=4', true, \[\], true, false, true, false);\_\_ez.queue.addFile('/detroitchicago/rochester.js', '/detroitchicago/rochester.js?gcb=195-18&cb=13', false, \['/detroitchicago/memphis.js','/detroitchicago/minneapolis.js'\], true, false, true, false);!function(){var e;\_\_ez.vep=(e=\[\],{Add:function(i,t){\_\_ez.dot.isDefined(i)&&\_\_ez.dot.isValid(t)&&e.push({type:"video",video\_impression\_id:i,domain\_id:\_\_ez.dot.getDID(),t\_epoch:\_\_ez.dot.getEpoch(0),data:\_\_ez.dot.dataToStr(t)})},Fire:function(){if(void 0===document.visibilityState||"prerender"!==document.visibilityState){if(\_\_ez.dot.isDefined(e)&&e.length>0)for(;e.length>0;){var i=5;i>e.length&&(i=e.length);var t=e.splice(0,i),o=\_\_ez.dot.getURL("/detroitchicago/grapefruit.gif")+"?orig="+(!0===\_\_ez.template.isOrig?1:0)+"&v="+btoa(JSON.stringify(t));\_\_ez.dot.Fire(o)}e=\[\]}}})}();!function(){function e(i){return e="function"==typeof Symbol&&"symbol"==typeof Symbol.iterator?function(e){return typeof e}:function(e){return e&&"function"==typeof Symbol&&e.constructor===Symbol&&e!==Symbol.prototype?"symbol":typeof e},e(i)}\_\_ez.pel=function(){var i=\[\];function t(t,o,d,\_,n,r,a,s){if(\_\_ez.dot.isDefined(t)&&0!=\_\_ez.dot.isAnyDefined(t.getSlotElementId,t.ElementId)){void 0===s&&(s=!1);var p=parseInt(\_\_ez.dot.getTargeting(t,"ap")),f=\_\_ez.dot.getSlotIID(t),u=\_\_ez.dot.getAdUnit(t,s),z=parseInt(\_\_ez.dot.getTargeting(t,"compid")),g=0,c=0,l=function(i){if("undefined"==typeof \_ezim\_d)return!1;var t=\_\_ez.dot.getAdUnitPath(i).split("/").pop();if("object"===("undefined"==typeof \_ezim\_d?"undefined":e(\_ezim\_d))&&\_ezim\_d.hasOwnProperty(t))return \_ezim\_d\[t\];for(var o in \_ezim\_d)if(o.split("/").pop()===t)return \_ezim\_d\[o\];return!1}(t);"object"==e(l)&&(void 0!==l.creative\_id&&(c=l.creative\_id),void 0!==l.line\_item\_id&&(g=l.line\_item\_id)),\_\_ez.dot.isDefined(f,u)&&\_\_ez.dot.isValid(o)&&("0"===f&&!0!==s||""===u||i.push({type:"impression",impression\_id:f,domain\_id:\_\_ez.dot.getDID(),unit:u,t\_epoch:\_\_ez.dot.getEpoch(0),revenue:d,est\_revenue:\_,ad\_position:p,ad\_size:"",bid\_floor\_filled:n,bid\_floor\_prev:r,stat\_source\_id:a,country\_code:\_\_ez.dot.getCC(),pageview\_id:\_\_ez.dot.getPageviewId(),comp\_id:z,line\_item\_id:g,creative\_id:c,data:\_\_ez.dot.dataToStr(o),is\_orig:s||\_\_ez.template.isOrig}))}}function o(){void 0!==document.visibilityState&&"prerender"===document.visibilityState||(\_\_ez.dot.isDefined(i)&&i.length>0&&\[i.filter((function(e){return e.is\_orig})),i.filter((function(e){return!e.is\_orig}))\].forEach((function(e){for(;e.length>0;){var i=e\[0\].is\_orig||!1,t=5;t>e.length&&(t=e.length);var o=e.splice(0,t),d=\_\_ez.dot.getURL("/porpoiseant/army.gif")+"?orig="+(!0===i?1:0)+"&sts="+btoa(JSON.stringify(o));(void 0!==window.isAmp&&isAmp||void 0!==window.ezWp&&ezWp)&&void 0!==window.\_ezaq&&\_ezaq.hasOwnProperty("domain\_id")&&(d+="&visit\_uuid="+\_ezaq.visit\_uuid),\_\_ez.dot.Fire(d)}})),i=\[\])}return{Add:t,AddAndFire:function(e,i){t(e,i,0,0,0,0,0),o()},AddAndFireOrig:function(e,i){t(e,i,0,0,0,0,0,!0),o()},AddById:function(e,t,o,d){var \_=e.split("/");if(\_\_ez.dot.isDefined(e)&&3===\_.length&&\_\_ez.dot.isValid(t)){var n=\_\[0\],r={type:"impression",impression\_id:\_\[2\],domain\_id:\_\_ez.dot.getDID(),unit:n,t\_epoch:\_\_ez.dot.getEpoch(0),pageview\_id:\_\_ez.dot.getPageviewId(),data:\_\_ez.dot.dataToStr(t),is\_orig:o||\_\_ez.template.isOrig};void 0!==d&&(r.revenue=d),i.push(r)}},Fire:o,GetPixels:function(){return i}}}()}();\_\_ez.queue.addFile('/detroitchicago/raleigh.js', '/detroitchicago/raleigh.js?gcb=195-18&cb=6', false, \[\], true, false, true, false);\_\_ez.queue.addFile('/detroitchicago/tampa.js', '/detroitchicago/tampa.js?gcb=195-18&cb=5', false, \[\], true, false, true, false); (function(){if("function"===typeof window.CustomEvent)return!1;window.CustomEvent=function(c,a){a=a||{bubbles:!1,cancelable:!1,detail:null};var b=document.createEvent("CustomEvent");b.initCustomEvent(c,a.bubbles,a.cancelable,a.detail);return b}})();\_\_ez.queue.addFile('/detroitchicago/tulsa.js', '/detroitchicago/tulsa.js?gcb=195-18&cb=7', false, \[\], true, false, true, false); window.dataLayer = window.dataLayer || \[\]; function gtag(){dataLayer.push(arguments);} gtag('js', new Date()); gtag('config', 'G-NLMVGQQTXB');    How to use Raspberry Pi as a Wireless Router with Firewall? – RaspberryTips    body{--wp--preset--color--black: #000000;--wp--preset--color--cyan-bluish-gray: #abb8c3;--wp--preset--color--white: #ffffff;--wp--preset--color--pale-pink: #f78da7;--wp--preset--color--vivid-red: #cf2e2e;--wp--preset--color--luminous-vivid-orange: #ff6900;--wp--preset--color--luminous-vivid-amber: #fcb900;--wp--preset--color--light-green-cyan: #7bdcb5;--wp--preset--color--vivid-green-cyan: #00d084;--wp--preset--color--pale-cyan-blue: #8ed1fc;--wp--preset--color--vivid-cyan-blue: #0693e3;--wp--preset--color--vivid-purple: #9b51e0;--wp--preset--gradient--vivid-cyan-blue-to-vivid-purple: linear-gradient(135deg,rgba(6,147,227,1) 0%,rgb(155,81,224) 100%);--wp--preset--gradient--light-green-cyan-to-vivid-green-cyan: linear-gradient(135deg,rgb(122,220,180) 0%,rgb(0,208,130) 100%);--wp--preset--gradient--luminous-vivid-amber-to-luminous-vivid-orange: linear-gradient(135deg,rgba(252,185,0,1) 0%,rgba(255,105,0,1) 100%);--wp--preset--gradient--luminous-vivid-orange-to-vivid-red: linear-gradient(135deg,rgba(255,105,0,1) 0%,rgb(207,46,46) 100%);--wp--preset--gradient--very-light-gray-to-cyan-bluish-gray: linear-gradient(135deg,rgb(238,238,238) 0%,rgb(169,184,195) 100%);--wp--preset--gradient--cool-to-warm-spectrum: linear-gradient(135deg,rgb(74,234,220) 0%,rgb(151,120,209) 20%,rgb(207,42,186) 40%,rgb(238,44,130) 60%,rgb(251,105,98) 80%,rgb(254,248,76) 100%);--wp--preset--gradient--blush-light-purple: linear-gradient(135deg,rgb(255,206,236) 0%,rgb(152,150,240) 100%);--wp--preset--gradient--blush-bordeaux: linear-gradient(135deg,rgb(254,205,165) 0%,rgb(254,45,45) 50%,rgb(107,0,62) 100%);--wp--preset--gradient--luminous-dusk: linear-gradient(135deg,rgb(255,203,112) 0%,rgb(199,81,192) 50%,rgb(65,88,208) 100%);--wp--preset--gradient--pale-ocean: linear-gradient(135deg,rgb(255,245,203) 0%,rgb(182,227,212) 50%,rgb(51,167,181) 100%);--wp--preset--gradient--electric-grass: linear-gradient(135deg,rgb(202,248,128) 0%,rgb(113,206,126) 100%);--wp--preset--gradient--midnight: linear-gradient(135deg,rgb(2,3,129) 0%,rgb(40,116,252) 100%);--wp--preset--duotone--dark-grayscale: url('#wp-duotone-dark-grayscale');--wp--preset--duotone--grayscale: url('#wp-duotone-grayscale');--wp--preset--duotone--purple-yellow: url('#wp-duotone-purple-yellow');--wp--preset--duotone--blue-red: url('#wp-duotone-blue-red');--wp--preset--duotone--midnight: url('#wp-duotone-midnight');--wp--preset--duotone--magenta-yellow: url('#wp-duotone-magenta-yellow');--wp--preset--duotone--purple-green: url('#wp-duotone-purple-green');--wp--preset--duotone--blue-orange: url('#wp-duotone-blue-orange');--wp--preset--font-size--small: 13px;--wp--preset--font-size--medium: 20px;--wp--preset--font-size--large: 36px;--wp--preset--font-size--x-large: 42px;--wp--preset--spacing--20: 0.44rem;--wp--preset--spacing--30: 0.67rem;--wp--preset--spacing--40: 1rem;--wp--preset--spacing--50: 1.5rem;--wp--preset--spacing--60: 2.25rem;--wp--preset--spacing--70: 3.38rem;--wp--preset--spacing--80: 5.06rem;}:where(.is-layout-flex){gap: 0.5em;}body .is-layout-flow > .alignleft{float: left;margin-inline-start: 0;margin-inline-end: 2em;}body .is-layout-flow > .alignright{float: right;margin-inline-start: 2em;margin-inline-end: 0;}body .is-layout-flow > .aligncenter{margin-left: auto !important;margin-right: auto !important;}body .is-layout-constrained > .alignleft{float: left;margin-inline-start: 0;margin-inline-end: 2em;}body .is-layout-constrained > .alignright{float: right;margin-inline-start: 2em;margin-inline-end: 0;}body .is-layout-constrained > .aligncenter{margin-left: auto !important;margin-right: auto !important;}body .is-layout-constrained > :where(:not(.alignleft):not(.alignright):not(.alignfull)){max-width: var(--wp--style--global--content-size);margin-left: auto !important;margin-right: auto !important;}body .is-layout-constrained > .alignwide{max-width: var(--wp--style--global--wide-size);}body .is-layout-flex{display: flex;}body .is-layout-flex{flex-wrap: wrap;align-items: center;}body .is-layout-flex > \*{margin: 0;}:where(.wp-block-columns.is-layout-flex){gap: 2em;}.has-black-color{color: var(--wp--preset--color--black) !important;}.has-cyan-bluish-gray-color{color: var(--wp--preset--color--cyan-bluish-gray) !important;}.has-white-color{color: var(--wp--preset--color--white) !important;}.has-pale-pink-color{color: var(--wp--preset--color--pale-pink) !important;}.has-vivid-red-color{color: var(--wp--preset--color--vivid-red) !important;}.has-luminous-vivid-orange-color{color: var(--wp--preset--color--luminous-vivid-orange) !important;}.has-luminous-vivid-amber-color{color: var(--wp--preset--color--luminous-vivid-amber) !important;}.has-light-green-cyan-color{color: var(--wp--preset--color--light-green-cyan) !important;}.has-vivid-green-cyan-color{color: var(--wp--preset--color--vivid-green-cyan) !important;}.has-pale-cyan-blue-color{color: var(--wp--preset--color--pale-cyan-blue) !important;}.has-vivid-cyan-blue-color{color: var(--wp--preset--color--vivid-cyan-blue) !important;}.has-vivid-purple-color{color: var(--wp--preset--color--vivid-purple) !important;}.has-black-background-color{background-color: var(--wp--preset--color--black) !important;}.has-cyan-bluish-gray-background-color{background-color: var(--wp--preset--color--cyan-bluish-gray) !important;}.has-white-background-color{background-color: var(--wp--preset--color--white) !important;}.has-pale-pink-background-color{background-color: var(--wp--preset--color--pale-pink) !important;}.has-vivid-red-background-color{background-color: var(--wp--preset--color--vivid-red) !important;}.has-luminous-vivid-orange-background-color{background-color: var(--wp--preset--color--luminous-vivid-orange) !important;}.has-luminous-vivid-amber-background-color{background-color: var(--wp--preset--color--luminous-vivid-amber) !important;}.has-light-green-cyan-background-color{background-color: var(--wp--preset--color--light-green-cyan) !important;}.has-vivid-green-cyan-background-color{background-color: var(--wp--preset--color--vivid-green-cyan) !important;}.has-pale-cyan-blue-background-color{background-color: var(--wp--preset--color--pale-cyan-blue) !important;}.has-vivid-cyan-blue-background-color{background-color: var(--wp--preset--color--vivid-cyan-blue) !important;}.has-vivid-purple-background-color{background-color: var(--wp--preset--color--vivid-purple) !important;}.has-black-border-color{border-color: var(--wp--preset--color--black) !important;}.has-cyan-bluish-gray-border-color{border-color: var(--wp--preset--color--cyan-bluish-gray) !important;}.has-white-border-color{border-color: var(--wp--preset--color--white) !important;}.has-pale-pink-border-color{border-color: var(--wp--preset--color--pale-pink) !important;}.has-vivid-red-border-color{border-color: var(--wp--preset--color--vivid-red) !important;}.has-luminous-vivid-orange-border-color{border-color: var(--wp--preset--color--luminous-vivid-orange) !important;}.has-luminous-vivid-amber-border-color{border-color: var(--wp--preset--color--luminous-vivid-amber) !important;}.has-light-green-cyan-border-color{border-color: var(--wp--preset--color--light-green-cyan) !important;}.has-vivid-green-cyan-border-color{border-color: var(--wp--preset--color--vivid-green-cyan) !important;}.has-pale-cyan-blue-border-color{border-color: var(--wp--preset--color--pale-cyan-blue) !important;}.has-vivid-cyan-blue-border-color{border-color: var(--wp--preset--color--vivid-cyan-blue) !important;}.has-vivid-purple-border-color{border-color: var(--wp--preset--color--vivid-purple) !important;}.has-vivid-cyan-blue-to-vivid-purple-gradient-background{background: var(--wp--preset--gradient--vivid-cyan-blue-to-vivid-purple) !important;}.has-light-green-cyan-to-vivid-green-cyan-gradient-background{background: var(--wp--preset--gradient--light-green-cyan-to-vivid-green-cyan) !important;}.has-luminous-vivid-amber-to-luminous-vivid-orange-gradient-background{background: var(--wp--preset--gradient--luminous-vivid-amber-to-luminous-vivid-orange) !important;}.has-luminous-vivid-orange-to-vivid-red-gradient-background{background: var(--wp--preset--gradient--luminous-vivid-orange-to-vivid-red) !important;}.has-very-light-gray-to-cyan-bluish-gray-gradient-background{background: var(--wp--preset--gradient--very-light-gray-to-cyan-bluish-gray) !important;}.has-cool-to-warm-spectrum-gradient-background{background: var(--wp--preset--gradient--cool-to-warm-spectrum) !important;}.has-blush-light-purple-gradient-background{background: var(--wp--preset--gradient--blush-light-purple) !important;}.has-blush-bordeaux-gradient-background{background: var(--wp--preset--gradient--blush-bordeaux) !important;}.has-luminous-dusk-gradient-background{background: var(--wp--preset--gradient--luminous-dusk) !important;}.has-pale-ocean-gradient-background{background: var(--wp--preset--gradient--pale-ocean) !important;}.has-electric-grass-gradient-background{background: var(--wp--preset--gradient--electric-grass) !important;}.has-midnight-gradient-background{background: var(--wp--preset--gradient--midnight) !important;}.has-small-font-size{font-size: var(--wp--preset--font-size--small) !important;}.has-medium-font-size{font-size: var(--wp--preset--font-size--medium) !important;}.has-large-font-size{font-size: var(--wp--preset--font-size--large) !important;}.has-x-large-font-size{font-size: var(--wp--preset--font-size--x-large) !important;} .wp-block-navigation a:where(:not(.wp-element-button)){color: inherit;} :where(.wp-block-columns.is-layout-flex){gap: 2em;} .wp-block-pullquote{font-size: 1.5em;line-height: 1.6;}     .entry-content a.lazy-load-youtube, a.lazy-load-youtube, .lazy-load-vimeo{ background-size: cover; }.titletext.youtube { display: none; }.lazy-load-div:before { content: "\\25B6"; text-shadow: 0px 0px 60px rgba(0,0,0,0.8); }     .search-wrapper #search-icon{background:url("https://raspberrytips.com/wp-content/themes/acabado/img/search-icon.png") center/cover no-repeat #fff;}.share-container .email-btn:before{background:url("https://raspberrytips.com/wp-content/themes/acabado/img/envelope.svg") center/cover no-repeat;}.share-container .print-btn:before{background:url("https://raspberrytips.com/wp-content/themes/acabado/img/print-icon.svg") center/cover no-repeat;}.externallinkimage{background-image:url("https://raspberrytips.com/wp-content/themes/acabado/img/extlink.png")}body, body ul, body li, body td, body th, body p, body p.legal-disclaimer, body input, body select, body optgroup, body textarea, body .entry-meta span, body.single .entry-meta .byline, .entry-content .woocommerce div.product .woocommerce-tabs ul.tabs li a{ color: #000000; }body.home #page .hero-text-wrapper h2.hero-text{ color:#ffffff; }#content h1, #content h2:not(.widget-title, .hero-text, .section-header-text, .card-title), #content h3, #content .author-card .author-info a, #content h4, #content h5, #content h6, #content .header { color: #c61e4a; }body.home #page h2.section-header-text,#page .featured-categories-wrapper .category-card h2:before{ background-color:#363940;}#page .featured-categories-wrapper .category-card:hover h2:before{ opacity:0.5; transition:opacity 500ms;}body a, body a:visited, body a:focus, body a:active{ color: #c61e4a; }body a:hover, body a:visited:hover, body a:focus, body a:active { color: #363940 }.woocommerce #respond input#submit, #content .wp-block-button\_\_link:not(.has-background), #content button:not(.hamburger, .toggle-submenu, .search-submit), #content a.button:not(.hamburger, .toggle-submenu, .search-submit), #content a.button:visited:not(.hamburger, .toggle-submenu, .search-submit), #content button:not(.hamburger, .toggle-submenu, .search-submit), #content input\[type='button'\]:not(.hamburger, .toggle-submenu, .search-submit), #content input\[type='reset'\], #content input\[type='submit'\], #content .button:not(.hamburger, .toggle-submenu, .search-submit) { background: #c61e4a; }.woocommerce #respond input#submit, .wp-block-button\_\_link:not(.has-text-color), #page button:not(.hamburger, .toggle-submenu, .search-submit), #page a.button:not(.hamburger, .toggle-submenu, .search-submit), #page a.button:visited:not(.hamburger, .toggle-submenu, .search-submit), input\[type='button'\]:not(.hamburger, .toggle-submenu, .search-submit), input\[type='reset'\], input\[type='submit'\], .button:not(.hamburger, .toggle-submenu, .search-submit) { color: #ffffff; }.woocommerce div.product .woocommerce-tabs ul.tabs::before, .woocommerce div.product .woocommerce-tabs ul.tabs li{border-color:#f0f0f0;}#content hr, body .wp-block-separator{ background-color: #f0f0f0; } #page aside#secondary .legal-info-container, #page aside#secondary .sidebar-ad{ border-top-color: #f0f0f0;} #page .author-card{border-top-color: #f0f0f0;border-bottom-color: #f0f0f0;}#page .site-footer{border-top-color: #f0f0f0;}@media (min-width: 960px){#page .site-content .widget-area{border-left-color:#f0f0f0;}}#page .main-navigation .nav-menu > li a{ color:#363940;} #page .main-navigation .nav-menu > li.menu-item-has-children > a:after{border-top-color:#363940;}#page .main-navigation ul ul.submenu{background:#fff;}#page .main-navigation ul ul.submenu a {color:#363940;} #page .main-navigation ul ul.submenu a:after{border-top-color:#363940;}#page .main-navigation ul ul.submenu li:hover{background:#818592;}#page .main-navigation ul ul.submenu li:hover>a {color:#fff;} #page .main-navigation ul ul.submenu li:hover > a:after{border-top-color:#fff;}#content #antibounce { background: #f0f0f0; }body #content #antibounce .antibounce-card .copy-wrapper p{ color: #000000; }body #content #antibounce .antibounce-card button{ background-color: #000000; }body #content #antibounce .antibounce-card button { color: #ffffff } #mlb2-1319480.ml-form-embedContainer .ml-form-embedWrapper.embedForm { max-width: 800px !important; } .article-card header p { font-weight: bold; font-size: 16px; } body.home .articles-wrapper>h2, .widget-title { text-transform: none; } aside#secondary .about-wrapper { padding: 20px 0 0px; } #footer-menu li.menu-item { list-style-type: none; display: inline-block; padding-left: 10px; } #footer-menu li.menu-item a { text-decoration: none; color: #bbbaba; } #footer-menu li.menu-item a:hover { text-decoration: underline; } body, p { color: #252525; } strong { font-weight: 700; } code, pre.EnlighterJSRAW, pre.wp-block-preformatted { border-left: 6px solid #C61E4A; background-color: #f0f0f1; padding: 10px; display: block; background-image: url(https://raspberrytips.fr/code.gif); } a:visited { color: #C61E4A; } .site-footer { border-top: 1px solid #f0f0f0; background-color: #3d3f40; } .site-info { letter-spacing: 1px; color: #bbbaba; text-transform: uppercase; font-size: 12px; } .legal-info-container p, .excerpt p { font-weight: normal; } #mlb2-1319480.ml-form-embedContainer .ml-form-embedWrapper .ml-form-embedBody .ml-form-horizontalRow button { width:180px; } #mlb2-1319480.ml-form-embedContainer { border: 2px #C61E4A dashed; } figcaption { font-size: 75%; margin-left: auto; margin-right: auto; width: 75%; } div.wpforms-container-full .wpforms-form button { background-color: #363636; padding: 10px; border-radius: 5px; } .externallinkimage { display: none; } .divbook { width:100%; padding:10px; } .borderbook { height: 100%; min-height: 150px; border: 2px #C61E4A dashed; border-radius:10px; background: #c61e4a40; } .imagebook { max-width: 25%; float: left; } .imagebook img { max-height: 120px; } .textbook { text-align: center; } .titlebook { font-weight: bold; font-size: 20px; } .buttonbook { padding-top: 10px; } #content .button, #content a.button { padding: 8px 8px; } .borderbook:after { content: ""; display: table; clear: both; } .wp-block-buttons { text-align:center; } .wp-polls .Buttons { color: white; border: 1px solid #363636; background-color: #C61E4A; } .ml\_form { width: 100%; border: 1px dotted black; text-align: center; background-color: #fdfdfd; padding: 10px; } .ml\_form\_input { margin: 10px; text-align: center; border-radius: 5px !important; } .ml\_title { font-size: 32px; font-weight: bold; } .ml\_text { font-size: 18px; } body, p, li { font-size: 1.2rem; } .article-card header p { font-size: 18px; } code { font-size: 1.1rem !important; } h1 { font-size: 2.25rem; } h2 { font-size: 2rem; } h3 { font-size: 1.75rem; } h4 { font-size: 1.5rem; } .divbookb { width:100%; padding:10px; } .borderbookb { height: 100%; min-height: 150px; border: 4px #C61E4A solid; border-radius:20px; background: #dd741b3b; } .imagebookb { max-width: 25%; float: left; } .imagebookb img { //max-height: 120px; padding:20px; } .textbookb { text-align: center; padding: 20px; } .titlebookb { font-weight: bold; font-size: 20px; } .buttonbookb { padding-top: 20px; } .buttonbookb .button { font-size: 1.3em !important; } .borderbookb:after { content: ""; display: table; clear: both; } /\* <!\[CDATA\[ \*/ var gainwpUAEventsData = {"options":{"event\_tracking":"1","event\_downloads":"zip|mp3\*|mpe\*g|pdf|docx\*|pptx\*|xlsx\*|rar\*","event\_bouncerate":0,"aff\_tracking":1,"event\_affiliates":"\\/out\\/","hash\_tracking":"1","root\_domain":"raspberrytips.com","event\_timeout":100,"event\_precision":0,"event\_formsubmit":1,"ga\_pagescrolldepth\_tracking":0,"ga\_with\_gtag":0}}; /\* \]\]> \*/ /\* <!\[CDATA\[ \*/ var tpbr\_settings = {"fixed":"fixed","user\_who":"notloggedin","guests\_or\_users":"guests","message":"BLACK FRIDAY SALE: Get 40% off through Nov 28th!","status":"active","yn\_button":"button","color":"#303030","button\_text":"Shop now","button\_url":"https:\\/\\/school.raspberrytips.com\\/?coupon=BLACKFRIDAY22","button\_behavior":"newwindow","is\_admin\_bar":"no","detect\_sticky":"0"}; /\* \]\]> \*/     @font-face { font-family: 'Libre Franklin Extra Bold'; src: url('https://raspberrytips.com/wp-content/plugins/patreon-connect/assets/fonts/librefranklin-extrabold-webfont.woff2') format('woff2'), url('https://raspberrytips.com/wp-content/plugins/patreon-connect/assets/fonts/librefranklin-extrabold-webfont.woff') format('woff'); font-weight: bold; }             (function(i,s,o,g,r,a,m){i\['GoogleAnalyticsObject'\]=r;i\[r\]=i\[r\]||function(){ (i\[r\].q=i\[r\].q||\[\]).push(arguments)},i\[r\].l=1\*new Date();a=s.createElement(o), m=s.getElementsByTagName(o)\[0\];a.async=1;a.src=g;m.parentNode.insertBefore(a,m) })(window,document,'script','https://www.google-analytics.com/analytics.js','ga'); ga('create', 'UA-122915905-1', 'auto'); ga('send', 'pageview'); var ezouid = "1"; var ezoTemplate = 'old\_site\_gc'; if(typeof ezouid == 'undefined') { var ezouid = 'none'; } var ezoFormfactor = '1'; var ezo\_elements\_to\_check = Array(); var soc\_app\_id = '0'; var did = 97361; var ezdomain = 'raspberrytips.com'; var ezoicSearchable = 1; var \_ezaq = {"ad\_cache\_level":0,"ad\_lazyload\_version":0,"ad\_load\_version":0,"city":"San Francisco","country":"US","days\_since\_last\_visit":-1,"domain\_id":97361,"domain\_test\_group":20230803,"engaged\_time\_visit":0,"ezcache\_level":1,"ezcache\_skip\_code":0,"form\_factor\_id":1,"framework\_id":1,"is\_return\_visitor":false,"is\_sitespeed":0,"last\_page\_load":"","last\_pageview\_id":"","lt\_cache\_level":0,"metro\_code":807,"page\_ad\_positions":"","page\_view\_count":0,"page\_view\_id":"1332ea45-4482-40b3-7a48-fba032ca80e6","position\_selection\_id":0,"postal\_code":"94124","pv\_event\_count":0,"response\_size\_orig":107915,"response\_time\_orig":126,"serverid":"34.221.24.17:5393","state":"CA","t\_epoch":1669383043,"template\_id":126,"time\_on\_site\_visit":0,"url":"https://raspberrytips.com/raspberry-pi-firewall/","user\_id":0,"word\_count":4333,"worst\_bad\_word\_level":0};var \_ezExtraQueries = "&ez\_orig=1"; function create\_ezolpl(pvID, rv) { var d = new Date(); d.setTime(d.getTime() + (365\*24\*60\*60\*1000)); var expires = "expires="+d.toUTCString(); \_\_ez.ck.setByCat("ezux\_lpl\_97361=" + new Date().getTime() + "|" + pvID + "|" + rv + "; " + expires, 3); } function attach\_ezolpl(pvID, rv) { if (document.readyState === "complete") { create\_ezolpl(pvID, rv); } if(window.attachEvent) { window.attachEvent("onload", create\_ezolpl, pvID, rv); } else { if(window.onload) { var curronload = window.onload; var newonload = function(evt) { curronload(evt); create\_ezolpl(pvID, rv); }; window.onload = newonload; } else { window.onload = create\_ezolpl.bind(null, pvID, rv); } } } \_\_ez.queue.addFunc("attach\_ezolpl", "attach\_ezolpl", \["1332ea45-4482-40b3-7a48-fba032ca80e6", "false"\], false, \['/detroitchicago/boise.js'\], true, false, false, false);   .video-container{overflow:hidden!important}.player-container{background:#1a1a1a!important;overflow:auto!important;width:900px!important;margin:0 0 20px!important}.ez-video-container{display:-webkit-box;display:-moz-box;display:-ms-flexbox;display:-webkit-flex;display:flex;flex-wrap:wrap}@media screen and (min-width:100px){.ez-video-container.ez-stuck{position:fixed;bottom:120px;z-index:999;right:20px;width:75%;height:auto;transform:translateY(100%);animation:fade-in-up .25s ease forwards}}@media screen and (min-width:768px){.ez-video-container.ez-stuck{position:fixed;bottom:120px;z-index:999;right:20px;width:55%;height:auto;transform:translateY(100%);animation:fade-in-up .25s ease forwards}}@media screen and (min-width:1024px){.ez-video-container.ez-stuck{position:fixed;bottom:120px;z-index:999;right:20px;margin-bottom:20px;width:30%;height:auto;transform:translateY(100%);animation:fade-in-up .75s ease forwards}}.ez-video-container.ez-stuck.vertical{width:225px;height:400px}.ez-video-container.ez-stuck.ez-float-left{right:auto;left:20px}.ez-video-container.ez-stuck.ez-float-center{right:auto;left:50%;margin-left:-130px}.ez-video-container.ez-stuck.ez-float-center.vertical{margin-left:-80px}.ez-video-ad-container{top:0;position:absolute;display:none;width:100%;height:100%}.ez-vad-controls{bottom:0;height:1.4em;position:absolute;overflow:hidden;display:none;opacity:1;background-color:#07141eb2;background:-moz-linear-gradient( bottom,rgba(7,20,30,.7) 0%,rgba(7,20,30,0) 100%);background:-webkit-gradient( linear,left bottom,left top,color-stop(0%,rgba(7,20,30,.7)),color-stop(100%,rgba(7,20,30,0)));background:-webkit-linear-gradient( bottom,rgba(7,20,30,.7) 0%,rgba(7,20,30,0) 100%);background:-o-linear-gradient(bottom,rgba(7,20,30,.7) 0%,rgba(7,20,30,0) 100%);background:-ms-linear-gradient(bottom,rgba(7,20,30,.7) 0%,rgba(7,20,30,0) 100%);background:linear-gradient(to top,rgba(7,20,30,.7) 0%,rgba(7,20,30,0) 100%);filter:progid:DXImageTransform.Microsoft.gradient( startColorstr='#0007141E',endColorstr='#07141E',GradientType=0 )}.ez-vad-controls.ez-vad-controls-showing{height:3.7em}.ez-vad-countdown{height:1em;color:#fff;text-shadow:0 0 .2em #000;cursor:default}.ez-vad-seek-bar{top:1.2em;height:.3em;position:absolute;background:#fff6}.ez-vad-progress{width:0;height:.3em;background-color:#ecc546}.ez-vad-play-pause,.ez-vad-mute,.ez-vad-slider,.ez-vad-fullscreen{width:2.33em;height:1.33em;top:.733em;left:0;position:absolute;color:#ccc;font-size:1.5em;line-height:2;text-align:center;font-family:VideoJS;cursor:pointer}.ez-vad-mute{left:auto;right:5.667em}.ez-vad-slider{left:auto;right:2.33em;width:3.33em;height:.667em;top:1.33em;background-color:#555}.ez-vad-slider-level{width:100%;height:.667em;background-color:#ecc546}.ez-vad-fullscreen{left:auto;right:0}.ez-vad-playing:before{content:"\\00f103"}.ez-vad-paused:before{content:"\\00f101"}.ez-vad-playing:hover:before,.ez-vad-paused:hover:before{text-shadow:0 0 1em #fff}.ez-vad-non-muted:before{content:"\\00f107"}.ez-vad-muted:before{content:"\\00f104"}.ez-vad-non-muted:hover:before,.ez-vad-muted:hover:before{text-shadow:0 0 1em #fff}.ez-vad-non-fullscreened:before{content:"\\00f108"}.ez-vad-fullscreened:before{content:"\\00f109"}.ez-vad-non-fullscreened:hover:before,.ez-vad-fullscreened:hover:before{text-shadow:0 0 1em #fff}.ez-video-wrap video{visibility:visible!important}.ez-wrap-float-only{height:0!important;width:0!important}.ez-playlist-float-only{display:none!important}.video-js .vjs-share\_\_middle{padding:0 0!important;width:80%}.video-js{float:left!important;font-size:10px;color:#fff;position:relative!important;width:100%;height:auto;margin:0}@keyframes fade-in-up{0%{opacity:0}100%{transform:translateY(0);opacity:1}}.floating-placeholder{background-color:#000;display:block}.floating-placeholder-sizer{width:100%;padding-bottom:56.25%}.ez-video-wrap{text-align:center;clear:both}.vjs-playlist{height:114px}.ez-video-link{margin-top:0px;margin-bottom:0px;margin-left:20px;margin-right:0px;font-size:16px;white-space:nowrap;overflow:hidden;text-overflow:ellipsis;display:block!important;text-align:left;max-width:90vw}  window.ezVideo = {"appendFloatAfterAd":false,"language":"en","titleString":"","titleOption":""}

[Skip to content](#content)

MENU

[![](https://raspberrytips.com/wp-content/uploads/2020/08/RaspberryTips-300x150.png)](https://raspberrytips.com/)  

[Search](#open)

.search-wrapper.search-active .search-field { width: 200px; display: inline-block; vertical-align: top; } .search-wrapper button\[type="submit"\] { display: inline-block; vertical-align: top; top: -35px; position: relative; background-color: transparent; height: 30px; width: 30px; padding: 0; margin: 0; background-image: url("https://raspberrytips.com/wp-content/themes/acabado/img/search-icon.png"); background-position: center; background-repeat: no-repeat; background-size: contain; } .search-wrapper.search-active button\[type="submit"\] { display: inline-block !important; } Search for: 

*   [Start Here](https://raspberrytips.com/start-here/)
*   [Products](https://raspberrytips.com/tm-school) Submenu Toggle
    *   [The Raspberry Pi Bootcamp](https://raspberrytips.com/tm-course)
    *   [Master Your Raspberry Pi In 30 Days](https://raspberrytips.com/tm-ebook)
    *   [Master Python On Raspberry Pi](https://raspberrytips.com/masterpython-tm)
*   [Community](https://raspberrytips.com/tm-community)
*   [Resources](https://raspberrytips.com/resources/?z=1)

[![](https://raspberrytips.com/wp-content/uploads/2022/11/nordvpn-bf22.png)](https://raspberrytips.com/nordvpn-bf22)

How to use Raspberry Pi as a Wireless Router with Firewall?
===========================================================

 Written by [Patrick Fromaget](https://raspberrytips.com/author/admin/)  in [How-To Tutorials](https://raspberrytips.com/category/how-to-tutorials/)

  

I wanted to build a router firewall on Raspberry Pi for a long time. I first tested Pfsense and OpenWRT with no success, and on a fresh Raspberry Pi OS I was missing information. But now it’s ok, I finally found how to do it, and I’ll share this with you

**The Raspberry Pi only have one Ethernet socket, so it’s not possible to create a firewall with two RJ45 interfaces.**  
**But there is a Wi-Fi interface that can be used for one side (LAN for example).**  
**One way to build a firewall is to use the hostapd and iptables services.**

And I’ll show you how. It’s a big topic with many services and network notions to understand.  
I’ll start with the theory and then explain how to install each software.

If you are looking to quickly progress on Raspberry Pi, [you can check out my e-book here](https://raspberrytips.com/book-intro). It’s a 30-day challenge, where you learn one new thing every day until you become a Raspberry Pi expert. The first third of the book teaches you the basics, but the following chapters include projects you can try on your own.

pfSense VMWare ESXi Installation an...

Please enable JavaScript

[pfSense VMWare ESXi Installation and Basic Wizard Configuration](https://humix.com/redirect?url=https%3A%2F%2F51sec.org%2Fhumix%2Fvideo%2F75a14af930054b1f02d62d8dbddd9efc6f75852c55bb0095a82036e505690e28)

Begin with the end in mind
--------------------------

### Router

**A router is a network device that connects two networks together.  
**If you have two Ethernet ports on a computer, with different networks on each, your computer can act as a router.

![router](https://raspberrytips.com/wp-content/uploads/2019/01/router.jpg)

In this schema, we have two different networks, connected with a router: 1.0 and 2.0.  
If the router is well configured, it allows A and B to see each other, while on a different network.

The Raspberry Pi have only one Ethernet card, but we can use the Wi-Fi card to create a second network.  
**So, the router part in this tutorial will allow us to connect the Wi-Fi network to the Ethernet network**.

### Firewall

**A firewall is a software. It allows us to add security policies in the router.  
**For instance, in the previous example, we can configure that A can ping B, but not access the HTTP server on B.  
I’ll use a software called “iptables” for this, but you can use any other firewall software if you prefer.

### My goal

If you use your Raspberry Pi at home, you probably don’t need to connect two networks.  
But **my goal is to create a new wireless access point with a firewall and other cool software to monitor the network and filter some kind of traffic**.

Here is my current network:

![my current network](https://raspberrytips.com/wp-content/uploads/2019/01/current-network.jpg)

And I want to turn it like this:

![](https://raspberrytips.com/wp-content/uploads/2019/01/new-network.jpg)

So, here are the steps you need to follow to do the same:

*   Install your Raspberry Pi on the network
*   Enable Wi-Fi access point with a different network subnet
*   Create a bridge between the two networks
*   Create firewall rules
*   Install other cool software

I’ll explain you each step in detail.  
Let’s move to the first step of this process 🙂

Install your Raspberry Pi
-------------------------

The first thing to do is to install your Raspberry Pi on the network:

*   **Install Raspberry Pi OS** by following [this tutorial](https://raspberrytips.com/install-raspbian-raspberry-pi/)  
    You don’t need the Desktop version, except if you want to use the Raspberry Pi for other things too
*   **Plug the Raspberry Pi on the network** with an RJ45 cable  
    We’ll use the Wi-Fi later, so you need to let him available
*   A static IP address is not mandatory but it can help  
    You can check the end of [this article](https://raspberrytips.com/find-current-ip-raspberry-pi/) to know how to configure it
*   Once done, **update your system** by doing:  
    `sudo apt update   sudo apt upgrade   sudo reboot`
*    **Enable SSH** in raspi-config > Interfacing options  
    `sudo raspi-config`  
    You’ll use it in this tutorial, to copy/paste command from this page.  
    You can find [more details on how to use SSH in this tutorial](https://raspberrytips.com/ssh-password-raspberry-pi/) if needed.

That’s it, you have done the preparation step, we can start with the router installation.

Are you a bit lost in the Linux command line? [Check this article first](https://raspberrytips.com/raspberry-pi-commands/), for the most important commands to remember, and a free downloadable cheat sheet so you can have the commands at your fingertips.

Get My Commands Cheat Sheet!  
Grab your free PDF file with all the commands you need to know on Raspberry Pi!  

  Download it now 

ga('send', 'event', 'Optins', 'display', 'Commands');

Install a wireless router
-------------------------

On Stretch (Debian 9), a script was available to do everything automatically, but it hadn’t been updated and doesn’t work anymore.  
So, we’ll do it manually, it’ not so complex.

### Configure the Wi-Fi country

If you are using a fresh new Raspberry Pi OS, you need to set a Wi-Fi country first.  
The Wi-Fi is disabled until that.

*   Open raspi-config  
    `sudo raspi-config`
*   Go to Localisation Options > Change WLAN country
*   Select your country in the list
*   Confirm and exit

### Install the services

We’ll mainly use two new services on our router:

*   **Hostapd**: to create the wireless access point
*   **DNSmasq**: to forward the DNS requests to another DNS server

Start by installing the required packages:  
`sudo apt install hostapd dnsmasq`

That’s it, we can now move to the configuration part.

### Configure Hostapd

In the Hostapd configuration file, we will add the settings for our new wireless network:

*   Open the configuration file:  
    `sudo nano /etc/hostapd/hostapd.conf`
*   Paste these lines (the file is probably empty):  
    `interface=wlan0   driver=nl80211   ssid=RaspberryTips-Wifi   hw_mode=g   channel=6   wmm_enabled=0   macaddr_acl=0   auth_algs=1   ignore_broadcast_ssid=0   wpa=2   wpa_passphrase=<YOURPASSWORD>   wpa_key_mgmt=WPA-PSK   wpa_pairwise=TKIP   rsn_pairwise=CCMP`  
    Don’t forget to set a passphrase, and you can edit the line you want (for example to use another channel, security level or SSID)
*   Save & exit (CTRL+O, CTRL+X)

Hostapd won’t start automatically on boot, there are two changes to do to enable this:

*   Edit the default configuration file:  
    `sudo nano /etc/default/hostapd`
*   Add this line at the end:  
    `DAEMON_CONF="/etc/hostapd/hostapd.conf"`
*   Save & Exit
*   Then, enable the service with:  
    `sudo systemctl unmask hostapd   sudo systemctl enable hostapd`

### Configure DNSmasq

The next step is to configure DNSmasq:

*   Open the configuration file:  
    `sudo nano /etc/dnsmasq.conf`
*   Paste these lines at the end:  
    `interface=wlan0   bind-dynamic   domain-needed   bogus-priv   dhcp-range=192.168.42.100,192.168.42.200,255.255.255.0,12h`  
    Nothing to change here, except if you want to change the subnet.
*   Save & exit (CTRL+O, CTRL+X)

### Configure the DHCP server

The last configuration file to change is the DHCP server, set it on the same subnet:

*   Open the configuration file:  
    `sudo nano /etc/dhcpcd.conf`
*   Scroll to the end of the file and paste these lines:  
    `nohook wpa_supplicant   interface wlan0   static ip_address=192.168.42.10/24   static routers=192.168.42.1`
*   Save & exit

We are almost ready for the first test.

### Enable IP forwarding

If you have several network cards, the default behavior on Linux is to isolate them.  
In our case, we want to enable the communication between the LAN and the Wi-Fi.  
So, we need to change this:

*   Open this file:  
    `sudo nano /etc/sysctl.conf`
*   Find this line (first page):  
    `#net.ipv4.ip_forward=1`
*   And uncomment it:  
    `net.ipv4.ip_forward=1`
*   Save & exit

You can now reboot for a first try:  
`sudo reboot`  
_Note: I had to do this two times on my two tests because I was not getting an IP address on the first reboot. No idea why…_

Once this is complete you should be able to see your Raspberry Pi access point in the networks list  
In your Wi-Fi networks list, you should see something like this:  
![wireless network](https://raspberrytips.com/wp-content/uploads/2019/01/unifi-wifi-ready.jpg)

**You can connect to it and check that everything is working as expected**.  
You should get an IP in the 192.168.42.0/24 subnet, the script created this network for you.  
You’ll not get any Internet connection for now, as we need to configure the firewall to allow the Internet traffic.

Understand the firewall concepts
--------------------------------

I’ll start with an introduction on the theory about firewall configuration.  
If you are already fluent with this, you can move on to the next section.

### Introduction

**The role of a firewall is to block or allow access from a specific IP to another.  
And often we also use a port to set the exact permission**.  
Ex: We deny port 22 to everyone, except computer A that can access computer B with port 22.

### Black or White

In a firewall configuration, you have the choice between two default rules:

*   **Blacklist**: Allow all except …
*   **Whitelist**: Deny all except …

Depending on what you want to do with your Raspberry Pi router, it’s your choice to take the one you want.  
The first option is probably ok if you are using it at home. You may want to block only certain things like the torrent protocol or specific IPs address.  
But at work it’s rather the second. The good practice is to block everything except what is allowed.

### In, Out and Forward

This one is easier.  
In your firewall, you can create rules in three directions:

*   **Input**: Network packets coming into the firewall
*   **Output**: Packets going out from the firewall
*   **Forward**: Packets going through the firewall

On a hosted web server, you can block anything in input except HTTP and HTTPS.  
But in output it’s not a big deal what your server is doing on the Internet.

**In our case, we’ll mainly use FORWARD rules only as there is nothing on the Raspberry Pi.  
**There is no need to protect it more than that.

Configure the firewall service
------------------------------

If you want, you can add a firewall in your router to filter the traffic.  
Maybe at home it’s not mandatory, but for a company or a public place you need this.

### IPTables

There are several firewall packages available on Raspberry Pi OS: iptables or ufw for example.  
There is also OpenWRT, a Raspberry Pi compatible distribution, to create a router firewall.

In this post, I’ll use iptables, the most used.  
It’s already installed on your Raspberry Pi, so there’s nothing else to do.

Get My Commands Cheat Sheet!  
Grab your free PDF file with all the commands you need to know on Raspberry Pi!  

  Download it now 

ga('send', 'event', 'Optins', 'display', 'Commands');

### See the current configuration

Before adding rules, you need to check the current configuration.  
To do this, use the command:  
`sudo iptables -L`

You should get something like that:

![](https://raspberrytips.com/wp-content/uploads/2020/06/iptables-empty.jpg)

We find the input, output and forward parts I talked about previously.  
**For each we see that the default policy is ACCEPT, so everything allowed except what we add (blacklist mode)**.

You can use this command later to check if the new rules you add correspond to what you want.

### Enable Internet forwarding

Before going into more details, we’ll just **add some basic rules to allow the Internet traffic:**

*   **Type these 3 commands:  
    **`sudo iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE   sudo iptables -A FORWARD -i eth0 -o wlan0 -m state --state RELATED,ESTABLISHED -j ACCEPT   sudo iptables -A FORWARD -i wlan0 -o eth0 -j ACCEPT`
*   You don’t need to understand them right now, I will explain everything in the next parts.  
    But once done, you should have an Internet access working on your access point.
*   **Here are the rules you have now, with iptables -L  
    **![iptables list current configuration](https://raspberrytips.com/wp-content/uploads/2019/01/iptables-list.jpg)

### Add a FORWARD rule

**We’ll use the iptables command to add new rules in the firewall.  
**Every network is different, so every firewall rules table is different.  
I’ll start by an example, and then I’ll give you the whole syntax to add specific rules in your environment.

*   **Start by resetting the iptables configuration**  
    `sudo iptables -F`  
    The order is important in the rules list, and as the router already accept everything in the forward section, we can’t block specific connections.
*   **Add a DROP rule**  
    `sudo iptables -A FORWARD -p tcp --dport 80 -j DROP`  
    This command specifies that:  
    – we add a new rule (**\-A**)  
    – in the forward section (**FORWARD**)  
    – for the tcp protocol (**\-p tcp**)  
    – for the HTTP port (**–dport 80**)  
    – and the action is to DROP everything (timeout connection)
*   **Use the 3 commands I gave you in the previous part to allow the other Internet traffic**
*   After that, you should not be able to access a website like [this one](http://ipset.netfilter.org/iptables.man.html) for example (but sites in HTTPS still work)

It’s ok, your first rule is operational.  
You can use iptables -F to remove all rules and start again.  
Or you can **use the same command with the -D operator instead of -A**.  
`sudo iptables -D FORWARD -p tcp --dport 80 -j DROP`

This command allows you to delete a specific rule and not all like with the -F.

### Iptables command syntax

As you should already understand, you can now use the same command template to create the firewall rules you need.

The command template is:  
`iptables -<operation> <direction> -p <protocol> --dport <port> -j <action>`

*   **operation**:
    *   \-F: flush, remove all rules, it requires no other parameters
    *   \-A: append, add a new rule
    *   \-D: delete, remove an existing rule
*   **direction**: INPUT, OUTPUT or FORWARD (see the previous section)
*   **protocol**: mainly TCP or UDP
*   **port**: the port number you want to create your rule for  
    You can find a [list of common ports here](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers)
*   **action**: Define the choice to make for the corresponding traffic
    *   ACCEPT: Allow access (while in whitelist mode)
    *   REJECT: Deny access and tell the sender it’s not allowed
    *   DROP: Deny access but don’t tell the sender

This is the short introduction to what you’ll mainly use.  
If you need further information, use “man iptables” or check [this page](https://linux.die.net/man/8/iptables) for all parameters.

### Switch to whitelist

As you can see with “iptables -L”, we are in blacklist mode: ACCEPT all except the rules we add.

If you are in a stricter environment, switch to whitelist mode.  
For example, if you are creating a free Wi-Fi in a hotel or other business, you probably want to allow only a few ports (like web and mails).

To do this, you need to create a list of all ports you want to allow.  
If you do all the commands manually, you’ll lose access after the first one 🙂  
So, the easiest way is to create a script that run all commands at once.

#### Create the firewall script

*   **Create a new file** with nano  
    `sudo nano /usr/local/bin/firewall.sh`
*   **Paste these lines** inside  
    `#!/bin/sh   #Clear all rules   iptables -F      #Whitelist mode   iptables -P INPUT ACCEPT   iptables -P FORWARD DROP   iptables -P OUTPUT ACCEPT      #Allow PING for everyone   iptables -A FORWARD -p icmp -j ACCEPT      #Allow HTTP/HTTPS for WiFi clients   iptables -A FORWARD -p tcp --dport 80 -j ACCEPT   iptables -A FORWARD -p tcp --dport 443 -j ACCEPT      #Allow POP/IMAP/SMTP for WiFi clients   iptables -A FORWARD -p tcp --dport 25 -j ACCEPT   iptables -A FORWARD -p tcp --dport 110 -j ACCEPT   iptables -A FORWARD -p tcp --dport 993 -j ACCEPT      #Allow PING for WiFi clients   iptables -A FORWARD -p icmp -j ACCEPT      #Allow NAT   iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE   iptables -A FORWARD -i eth0 -o wlan0 -m state --state RELATED,ESTABLISHED -j ACCEPT`

*   You can **adapt these lines to your needs**  
    This is just an example  
    I don’t drop on INPUT and OUTPUT in this sample script, but you can do it if you want a better control on your network usage
*   **Save and exit** (CTRL+O, CTRL+X)
*   **Add execution right to this script**  
    `sudo chmod +x firewall.sh`
*   **Run it  
    **`sudo /usr/local/bin/firewall.sh`
*   **Check if everything works fine  
    **If something goes wrong, reboot the Raspberry Pi to recover all access  
    Then find what you miss in your script

When it’s ok, you can add it in the init tab to start it on boot

### Make your configuration persistent

The GitHub script we installed before uses the file /etc/iptables.ipv4.nat to save the configuration  
So once it’s working, you can save your current configuration inside :

sudo iptables-save > /etc/iptables.ipv4.nat

This will load the configuration file on load and apply directly the changes

Monitor the network
-------------------

Now that the router is working (with a firewall or not), we can add other packages to improve the Raspberry Pi capabilities  
In this part, I suggest adding a web interface to monitor what happens on the Raspberry Pi (and on the network)

### What’s this tool?

The tool I chose is Webmin  
It’s a web interface, easy to install, that shows you all the current configuration, and several statistics and graphs about the system usage  
You can even change the configuration from this interface

If you know other ones tell me [in the community](https://raspberrytips.com/community)  
It’s a tool that exists for a long time, but I don’t know a more recent one to do this

### Webmin Installation

*   **Check the latest Webmin version** from [this page](http://www.webmin.com/download.html) (Source file)
*   **Download the file** like this:  
    `wget https://prdownloads.sourceforge.net/webadmin/webmin-1.941.tar.gz`
*   **Extract the archive** and move to the new folder  
    `tar -zxvf webmin-1.941.tar.gz cd webmin-1.941`
*   **Run the setup**  
    `sudo ./setup.sh /usr/local/webmin`  
    Keep all the default values  
    Set a password and choose if you want to use SSL or not  
    Wait a few seconds for the installation to finish
*   **The tool is now available at http://<IP>:10000**  
    Log in with the user name and password you just created

### Webmin interface

**I let you discover the web interface and browse through the menu  
**There are A LOT of tools inside, we don’t need all of this  
We’ll mainly use those in the “Networking” part

For example, you can enable bandwidth monitoring or manage your firewall configuration from here

![webmin](https://raspberrytips.com/wp-content/uploads/2019/01/webmin.jpg)

We’ll come back later to this interface, for the proxy configuration for example  
It’s the next part

Add a proxy and a web filter
----------------------------

### What’s a proxy?

A proxy has three main roles:

*   Creating a cache of all Internet pages, to increase web browsing speed
*   Log all pages, to generate reports (top domain, top traffic, …)
*   And we can add a website blocker, to deny access to some kinds of content

To do this, we’ll install Squid (the proxy) and SquidGuard (the filter) on the Raspberry Pi

### Squid installation

*   Squid is available in the repository. **Install it with**:  
    `sudo apt install squid`
*   **Backup the configuration file**:  
    `cd /etc/squid`  
    `sudo mv squid.conf squid.conf.old`
*   **Switch to the root user** a few seconds and **remove all the comments quickly**  
    `sudo su   cat squid.conf.old | egrep -v -e '^[[:blank:]]*#' | grep "\S" > squid.conf   exit`  
    Then **edit the configuration file**:  
    `sudo nano squid.conf`
*   And **add these lines at the beginning**  
    `acl LocalNet src 192.168.42.0/24   http_access allow LocalNet`  
    Squid works only on HTTP for the Wi-Fi network (42.X)
*   **Restart Squid** to apply changes  
    `sudo systemctl restart squid`

Once Squid is configured, you have two choices to use it:

*   **Configure your web browser to use the Raspberry Pi as the HTTP Proxy**  
    It depends on your browser, but you should find this option in Options > Network settings
*   **Configure iptables** to redirect automatically all HTTP traffic to squid  
    It should be something like this:    
    `iptables -t nat -A PREROUTING -i wlan0 -p tcp --dport 80 -j DNAT --to 192.168.42.1:3128   iptables -t nat -A PREROUTING -i eth0 -p tcp --dport 80 -j REDIRECT --to-port 3128`

Then check that HTTP websites are working fine  
You can see all the websites visited in the Squid log file :

sudo tail -f /var/log/squid/access.log

#### Webmin add-on

There is a Webmin add-on called “calamaris” you can install to monitor the proxy efficiency  
Install it with apt:

sudo apt install calamaris

And then go back to webmin, in the unused modules to find new tools for squid monitoring

### SquidGuard installation

We can now move to the SquidGuard installation:

*   **Install the squidguard package  
    **`sudo apt install squidguard`
*   **Download a list of websites by category  
    **`wget http://squidguard.mesd.k12.or.us/blacklists.tgz`
*   **Extract files from the archive  
    **`tar -zxvf blacklists.tgz`  
    While extracting, you’ll see some blacklist categories appear on your screen  
    You can choose one and use it for the SquidGuard configuration later  
    You can open the files to get some websites examples
*   **Move files to the SquidGuard folder  
    **`sudo mv blacklists /var/lib/squidguard/db`
*   **Archive the original SquidGuard configuration file  
    **`cd /etc/squiguard   mv squidGuard.conf squidGuard.conf.old`
*   **Create a new configuration file  
    **`sudo nano squidGuard.conf`
*   **Paste these lines  
    **`dbhome /var/lib/squidguard/db logdir /var/log/squidguard dest violence {   domainlist blacklists/violence/domains   urllist blacklists/violence/urls   log violenceaccess   }   acl {   default   {   pass !violence   redirect http://localhost/block.html   } }`  
    This is a sample file, you can block whatever you want  
    You can also add more categories by creating more dest sections
*   **Save and exit** (CTRL+O, CTRL+X)
*   **Build the SquidGuard database  
    **`sudo squidGuard -C all -d`  
    This can take a long time. If it’s too long, remove files you don’t need from the blacklists folder  
    Use a screen if you don’t stay in front of your computer (screen -S build)  
    So if the SSH connection with your computer is lost, this will not stop the build process
*   **Restart Squid to apply changes  
    **`sudo service squid restart`

It should be ok now, try to access a URL from the domain list and check that you are blocked by squidGuard

Related questions
-----------------

**Is it possible to add an Ad Blocker brick in this router?** Yes, you can use Pi-Hole to do this, it’s easy to install and you just need to set the Raspberry Pi as your DNS server (manually or in the DHCP configuration file, see Firewall > DNS issues for more information)

**Is it possible to use a Raspberry to build a “full Ethernet” router?** Yes, you can add an Ethernet hat to your Raspberry Pi like this expansion Hat ([more details on Amazon](https://www.amazon.com/dp/B07X1BH5FN/)). It’s perfect for a firewall.

Get My Commands Cheat Sheet!  
Grab your free PDF file with all the commands you need to know on Raspberry Pi!  

  Download it now 

ga('send', 'event', 'Optins', 'display', 'Commands');

**Reminder:** Remember that [all the members of my community](https://raspberrytips.com/community) get access to this website without ads, exclusive courses and much more. You can become part of this community for as little as $5 per month & get all the benefits immediately.

**You may also like:**

*   [25 awesome Raspberry Pi project ideas at home](https://raspberrytips.com/raspberry-pi-projects-for-home/?related)
*   [15 best operating systems for Raspberry Pi (with pictures)](https://raspberrytips.com/best-os-for-raspberry-pi/?related)
*   [My book: Master your Raspberry Pi in 30 days](https://raspberrytips.com/book-link)

Conclusion
----------

That’s it, you should now have better knowledge on how to build a complete firewall router with proxy on a Raspberry Pi

I hope it’s working for you.  
It took me a lot of time to write this post with many tests I didn’t include here, but you have the most important things, with the best tools  
If you have any issues, ask your question [in the community](https://raspberrytips.com/community), we’ll try to help you

Also, these tools are basically Linux stuff and you can find a lot of help on the Internet to go further

I give you all the documentation links here if needed:

*   [RPI Wifi router](https://github.com/harryallerston/RPI-Wireless-Hotspot)
*   [Iptables](https://netfilter.org/documentation/)
*   [Squid](http://www.squid-cache.org/Doc/)
*   [SquidGuard](http://squidguard.org/Doc/)
*   [Pi Hole](https://github.com/pi-hole/pi-hole/#one-step-automated-install)

Get My Commands Cheat Sheet!  
Grab your free PDF file with all the commands you need to know on Raspberry Pi!  

  Download it now 

ga('send', 'event', 'Optins', 'display', 'Commands');

**Additional Resources**
------------------------

**Not sure where to start?  
**Understand everything about the Raspberry Pi, stop searching for help all the time, and finally enjoy completing your projects.  
[Watch the Raspberry Pi Bootcamp course now](https://raspberrytips.com/school-course).  
  
**Master your Raspberry Pi in 30 days  
**Don’t want the basic stuff only? If you are looking for the best tips to become an expert on Raspberry Pi, this book is for you. Learn useful Linux skills and practice multiple projects with step-by-step guides.  
[Download the e-book](https://raspberrytips.com/school-ebook).  
  
**VIP Community**  
If you just want to hang out with me and other Raspberry Pi fans, you can also join the community. I share exclusive tutorials and behind-the-scenes content there. Premium members can also visit the website without ads.  
[More details here.  
](https://raspberrytips.com/community)  
**Need help building something with Python?**  
Create, understand and improve any Python script for your Raspberry Pi.  
Learn the essentials, step-by-step, without losing time understanding useless concepts.  
[Get the e-book now.](https://raspberrytips.com/masterpython-eb)  
  
You can also find all my recommendations for tools and hardware [on this page](https://raspberrytips.com/resources/?e=1).

{"@context":"http:\\/\\/schema.org\\/","@type":"BlogPosting","name":"How to use Raspberry Pi as a Wireless Router with Firewall?","url":"https:\\/\\/raspberrytips.com\\/raspberry-pi-firewall\\/","articleBody":"I wanted to build a router firewall on Raspberry Pi for a long time. I first tested Pfsense and OpenWRT&nbsp;with no success, and on a fresh Raspberry Pi OS I was missing information. But now it's ok, I finally found how to do it, and I'll share this with you\\n\\n\\n\\nThe Raspberry Pi only have one Ethernet socket, so it's not possible to create a firewall with two RJ45 interfaces. But there is a Wi-Fi interface that can be used for one side (LAN for example).One way to build a firewall is to use the hostapd and iptables services.\\n\\n\\n\\nAnd I'll show you how. It's a big topic with many services and network notions to understand.I'll start with the theory and then explain how to install each software.\\n\\n\\n\\n\\n\\nBegin with the end in mind\\n\\n\\n\\nRouter\\n\\n\\n\\nA router is a network device that connects two networks together.If you have two Ethernet ports on a computer, with different networks on each, your computer can act as a router.\\n\\n\\n\\n\\n\\n\\n\\nIn this schema, we have two different networks, connected with a router: 1.0 and 2.0.If the router is well configured, it allows A and B to see each other, while on a different network.\\n\\n\\n\\nThe Raspberry Pi have only one Ethernet card, but we can use the Wi-Fi card to create a second network.So, the router part in this tutorial will allow us to connect the Wi-Fi network to the Ethernet network.\\n\\n\\n\\nFirewall\\n\\n\\n\\nA firewall is a software. It allows us to add security policies in the router.For instance, in the previous example, we can configure that A can ping B, but not access the HTTP server on B.I'll use a software called \\"iptables\\" for this,&nbsp;but you can use any other firewall software if you prefer.\\n\\n\\n\\nMy goal\\n\\n\\n\\nIf you use your Raspberry Pi at home, you probably don't need to connect two networks.But my goal is to create a new wireless access point with a firewall and other cool software to monitor the network and filter some&nbsp;kind of traffic.\\n\\n\\n\\nHere is my current network:\\n\\n\\n\\n\\n\\n\\n\\nAnd I want to turn it like this:\\n\\n\\n\\n\\n\\n\\n\\nSo, here are the steps you need to follow to do the same:\\n\\n\\n\\nInstall your Raspberry Pi on the networkEnable Wi-Fi access point with a different network subnetCreate a bridge between the two networksCreate firewall rulesInstall other cool software\\n\\n\\n\\nI'll explain you each step&nbsp;in detail.Let's move to the first step of this process :)\\n\\n\\n\\nInstall your Raspberry Pi\\n\\n\\n\\nThe first thing to do is to install your Raspberry Pi on the network:\\n\\n\\n\\nInstall Raspberry Pi OS by following this tutorialYou don't need the Desktop version, except if you want to use the Raspberry Pi for other things tooPlug the Raspberry Pi on the network with an RJ45 cableWe'll use the Wi-Fi later, so you need to let him availableA static IP address is not mandatory but it can helpYou can check the end of this article to know how to configure itOnce done, update your system by doing: sudo apt update sudo apt upgrade sudo reboot &nbsp;Enable SSH in raspi-config &gt; Interfacing options sudo raspi-config You'll use it in this tutorial, to copy\\/paste command from this page.You can find more details on how to use SSH in this tutorial if needed.\\n\\n\\n\\nThat's it, you have done the preparation step, we can start with the router installation.\\n\\n\\n\\n\\n\\nInstall a wireless router\\n\\n\\n\\nOn Stretch (Debian 9), a script was available to do everything automatically, but it hadn't been updated and doesn't work anymore.So, we'll do it manually, it' not so complex.\\n\\n\\n\\nConfigure the Wi-Fi country\\n\\n\\n\\nIf you are using a fresh new Raspberry Pi OS, you need to set a Wi-Fi country first.The Wi-Fi is disabled until that.\\n\\n\\n\\nOpen raspi-configsudo raspi-configGo to Localisation Options &gt; Change WLAN countrySelect your country in the listConfirm and exit\\n\\n\\n\\nInstall the services\\n\\n\\n\\nWe'll mainly use two new services on our router:\\n\\n\\n\\nHostapd: to create the wireless access pointDNSmasq: to forward the DNS requests to another DNS server\\n\\n\\n\\nStart by installing the required packages:sudo apt install hostapd dnsmasq\\n\\n\\n\\nThat's it, we can now move to the configuration part.\\n\\n\\n\\nConfigure Hostapd\\n\\n\\n\\nIn the Hostapd configuration file, we will add the settings for our new wireless network:\\n\\n\\n\\nOpen the configuration file:sudo nano \\/etc\\/hostapd\\/hostapd.confPaste these lines (the file is probably empty):interface=wlan0driver=nl80211ssid=RaspberryTips-Wifihw\_mode=gchannel=6wmm\_enabled=0macaddr\_acl=0auth\_algs=1ignore\_broadcast\_ssid=0wpa=2wpa\_passphrase=&lt;YOURPASSWORD&gt;wpa\_key\_mgmt=WPA-PSKwpa\_pairwise=TKIPrsn\_pairwise=CCMPDon't forget to set a passphrase, and you can edit the line you want (for example to use another channel, security level or SSID)Save &amp; exit (CTRL+O, CTRL+X)\\n\\n\\n\\nHostapd won't start automatically on boot, there are two changes to do to enable this:\\n\\n\\n\\nEdit the default configuration file:sudo nano \\/etc\\/default\\/hostapdAdd this line at the end:DAEMON\_CONF=\\"\\/etc\\/hostapd\\/hostapd.conf\\"Save &amp; ExitThen, enable the service with:sudo systemctl unmask hostapdsudo systemctl enable hostapd\\n\\n\\n\\nConfigure DNSmasq\\n\\n\\n\\nThe next step is to configure DNSmasq:\\n\\n\\n\\nOpen the configuration file:sudo nano \\/etc\\/dnsmasq.confPaste these lines at the end:interface=wlan0bind-dynamicdomain-neededbogus-privdhcp-range=192.168.42.100,192.168.42.200,255.255.255.0,12hNothing to change here, except if you want to change the subnet.Save &amp; exit (CTRL+O, CTRL+X)\\n\\n\\n\\nConfigure the DHCP server\\n\\n\\n\\nThe last configuration file to change is the DHCP server, set it on the same subnet:\\n\\n\\n\\nOpen the configuration file:sudo nano \\/etc\\/dhcpcd.confScroll to the end of the file and paste these lines:nohook wpa\_supplicantinterface wlan0static ip\_address=192.168.42.10\\/24static routers=192.168.42.1Save &amp; exit\\n\\n\\n\\nWe are almost ready for the first test.\\n\\n\\n\\nEnable IP forwarding\\n\\n\\n\\nIf you have several network cards, the default behavior on Linux is to isolate them.In our case, we want to enable the communication between the LAN and the Wi-Fi.So, we need to change this:\\n\\n\\n\\nOpen this file:sudo nano \\/etc\\/sysctl.confFind this line (first page):#net.ipv4.ip\_forward=1And uncomment it:net.ipv4.ip\_forward=1Save &amp; exit\\n\\n\\n\\nYou can now reboot for a first try:sudo rebootNote: I had to do this two times on my two tests because I was not getting an IP address on the first reboot. No idea why...\\n\\n\\n\\nOnce this is complete you should be able to see your Raspberry Pi access point in the networks listIn your Wi-Fi networks list, you should&nbsp;see something like this:\\n\\n\\n\\nYou can connect to it and check that everything is working as expected.You should get an IP in the 192.168.42.0\\/24 subnet, the script created this network for you.You'll not get any Internet connection for now, as we need to configure the firewall to allow the Internet traffic.\\n\\n\\n\\nUnderstand the firewall concepts\\n\\n\\n\\nI'll start with an introduction on the theory about firewall configuration.If you are already fluent with this, you can move on to the next section.\\n\\n\\n\\nIntroduction\\n\\n\\n\\nThe role of a firewall is to block or allow access from a specific IP to another.And often we also use a port to set the exact permission.Ex: We&nbsp;deny port 22 to everyone, except computer A that can access computer B with port 22.\\n\\n\\n\\nBlack or White\\n\\n\\n\\nIn a firewall configuration, you have the choice between two default rules:\\n\\n\\n\\nBlacklist: Allow all except&nbsp;...Whitelist: Deny all except ...\\n\\n\\n\\nDepending on what you want to do with your Raspberry Pi router, it's your choice to take the one you want.The first option is probably ok if you are using it at home. You may want to block only certain things like the&nbsp;torrent protocol or specific IPs address.But at work it's rather the second. The good practice is to block everything except what&nbsp;is allowed.\\n\\n\\n\\nIn, Out and Forward\\n\\n\\n\\nThis one is easier.In your firewall, you can create rules in three directions:\\n\\n\\n\\nInput: Network packets coming into the firewallOutput: Packets going out from the firewallForward: Packets going through the firewall\\n\\n\\n\\nOn a hosted web server, you can block anything in input except HTTP and HTTPS.But in output it's not a big deal what your server is doing on the Internet.\\n\\n\\n\\nIn our case, we'll mainly use FORWARD rules only as there is nothing on the Raspberry Pi.There is no need to protect it more than that.\\n\\n\\n\\nConfigure the firewall service\\n\\n\\n\\nIf you want, you can add a firewall in your router to filter the traffic.Maybe at home it's not mandatory, but for a company or a public place you need this.\\n\\n\\n\\nIPTables\\n\\n\\n\\nThere are several firewall packages available on Raspberry Pi OS: iptables or ufw for example.There is also OpenWRT, a Raspberry Pi compatible distribution, to create a router firewall.\\n\\n\\n\\nIn this post, I'll use iptables, the most used.It's already installed on your Raspberry Pi, so there's nothing else to do.\\n\\n\\n\\nSee the current configuration\\n\\n\\n\\nBefore adding rules, you need to check the current configuration.To do this, use the command:sudo iptables -L\\n\\n\\n\\nYou should get something like that:\\n\\n\\n\\n\\n\\n\\n\\nWe find the input, output and forward parts I talked about previously.For each we see that the default policy is ACCEPT, so everything allowed except what we add (blacklist mode).\\n\\n\\n\\nYou can use this command later to check if the new rules you add correspond to what you want.\\n\\n\\n\\nEnable Internet forwarding\\n\\n\\n\\nBefore going into more details, we'll just add some basic rules to allow the Internet traffic:\\n\\n\\n\\nType these 3 commands:sudo iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADEsudo iptables -A FORWARD -i eth0 -o wlan0 -m state --state RELATED,ESTABLISHED -j ACCEPTsudo iptables -A FORWARD -i wlan0 -o eth0 -j ACCEPTYou don't need to understand them right now, I will explain everything in the next parts.But once done, you should have an Internet access working on your access point.Here are the rules you have now, with iptables -L\\n\\n\\n\\nAdd a FORWARD rule\\n\\n\\n\\nWe'll use the iptables command to add new rules in the firewall.Every network is different, so every firewall rules table is different.I'll start by an example, and then I'll give you the whole syntax to add specific rules in your environment.\\n\\n\\n\\nStart by resetting the iptables configuration sudo iptables -F The order is important in the rules list, and as the router already accept everything in the forward section, we can't block specific connections.Add a DROP rule sudo iptables -A FORWARD -p tcp --dport 80 -j DROP This command specifies that:- we add a new rule (-A)- in the forward section (FORWARD)- for the tcp protocol (-p tcp)- for the HTTP port (--dport 80)- and the action is to DROP everything (timeout connection) Use the 3 commands I gave you in the previous part to allow the other Internet trafficAfter that, you should not be able to access a website like this one for example (but sites in HTTPS still work)\\n\\n\\n\\nIt's ok, your first rule is operational.You can use iptables -F to&nbsp;remove all rules and start again.Or you can use the same command with the -D operator instead of -A.sudo iptables -D FORWARD -p tcp --dport 80 -j DROP\\n\\n\\n\\nThis command allows you to delete a specific rule and not all like with the -F.\\n\\n\\n\\nIptables command syntax\\n\\n\\n\\nAs you should&nbsp;already understand, you can now use the same command template to create the firewall rules you need.\\n\\n\\n\\nThe command template is:iptables -&lt;operation&gt; &lt;direction&gt; -p &lt;protocol&gt; --dport &lt;port&gt; -j &lt;action&gt;\\n\\n\\n\\noperation: -F: flush, remove all rules, it requires no other parameters-A: append, add a new rule-D: delete, remove an existing rule direction: INPUT, OUTPUT or FORWARD (see the previous section)protocol: mainly TCP or UDPport: the port number you want to create your rule forYou can find a list of common ports hereaction: Define the choice to make for the corresponding traffic ACCEPT: Allow access (while in whitelist mode)REJECT: Deny access and tell&nbsp;the sender it's not allowedDROP: Deny access but don't tell the sender \\n\\n\\n\\nThis is the short introduction to what you'll mainly use.If you need further information, use \\"man iptables\\" or check this page&nbsp;for all parameters.\\n\\n\\n\\nSwitch to whitelist\\n\\n\\n\\nAs you can see with \\"iptables -L\\", we are in blacklist mode: ACCEPT all except the rules we add.\\n\\n\\n\\nIf you are in a stricter environment, switch to whitelist mode.For example,&nbsp;if you are creating a free Wi-Fi in a hotel or other business, you probably want to allow only a few ports (like web and mails).\\n\\n\\n\\nTo do this, you need to create a list of all ports you want to allow.If you do all the commands manually, you'll lose access after the first one :)So, the easiest way is to create a script that run all commands at once.\\n\\n\\n\\nCreate the firewall script\\n\\n\\n\\nCreate a new file with nano sudo nano \\/usr\\/local\\/bin\\/firewall.sh Paste these lines inside #!\\/bin\\/sh #Clear all rules iptables -F #Whitelist mode iptables -P INPUT ACCEPT iptables -P FORWARD DROP iptables -P OUTPUT ACCEPT #Allow PING for everyone iptables -A FORWARD -p icmp -j ACCEPT #Allow HTTP\\/HTTPS for WiFi clients iptables -A FORWARD -p tcp --dport 80 -j ACCEPT iptables -A FORWARD -p tcp --dport 443 -j ACCEPT#Allow POP\\/IMAP\\/SMTP for WiFi clients iptables -A FORWARD -p tcp --dport 25 -j ACCEPT iptables -A FORWARD -p tcp --dport 110 -j ACCEPT iptables -A FORWARD -p tcp --dport 993 -j ACCEPT #Allow PING for WiFi clients iptables -A FORWARD -p icmp -j ACCEPT#Allow NATiptables -t nat -A POSTROUTING -o eth0 -j MASQUERADEiptables -A FORWARD -i eth0 -o wlan0 -m state --state RELATED,ESTABLISHED -j ACCEPT\\n\\n\\n\\nYou can adapt these lines to your needsThis is just an exampleI don't drop on INPUT and OUTPUT in this sample script, but you can do it if you want a better control on your network usage Save and exit (CTRL+O, CTRL+X)Add execution right to this script sudo chmod +x firewall.sh Run it sudo \\/usr\\/local\\/bin\\/firewall.sh Check if everything works fineIf something goes wrong, reboot the Raspberry Pi to recover all accessThen find what you miss in your script\\n\\n\\n\\nWhen it's ok, you can add it in the init tab to start it on boot\\n\\n\\n\\nMake your configuration persistent\\n\\n\\n\\nThe GitHub script we installed before uses the file&nbsp;\\/etc\\/iptables.ipv4.nat to save the configurationSo once it's working, you can save your current configuration inside&nbsp;:\\n\\n\\n\\nsudo iptables-save &gt; \\/etc\\/iptables.ipv4.nat\\n\\n\\n\\nThis will load the configuration file on load and apply directly the changes\\n\\n\\n\\nMonitor the network\\n\\n\\n\\nNow that the router is working (with a firewall or not), we can add other packages to improve the Raspberry Pi capabilitiesIn this part, I suggest adding a web interface to monitor what happens on the Raspberry Pi (and on the network)\\n\\n\\n\\nWhat's this tool?\\n\\n\\n\\nThe tool I chose is WebminIt's a web interface, easy to install, that shows you all the current configuration, and several statistics and graphs about the system usageYou can even change the configuration from this interface\\n\\n\\n\\nIf you know other ones tell me in the communityIt's a tool that exists for a long time, but I don't know a more recent one to do this\\n\\n\\n\\nWebmin Installation\\n\\n\\n\\nCheck the latest Webmin version from this page (Source file)Download the file like this: wget https:\\/\\/prdownloads.sourceforge.net\\/webadmin\\/webmin-1.941.tar.gzExtract the archive and move to the new folder tar -zxvf webmin-1.941.tar.gz cd webmin-1.941 Run the setup sudo&nbsp;.\\/setup.sh \\/usr\\/local\\/webmin Keep all the default valuesSet a password and choose if you want to use SSL or notWait a few seconds for the installation to finish The tool is now available at http:\\/\\/&lt;IP&gt;:10000Log in with the user name and password you&nbsp;just&nbsp;created\\n\\n\\n\\nWebmin interface\\n\\n\\n\\nI let you discover the web interface and browse through the menuThere are A LOT of tools inside, we don't need all of thisWe'll mainly use those in the \\"Networking\\" part\\n\\n\\n\\nFor example, you can enable bandwidth monitoring or manage your firewall configuration from here\\n\\n\\n\\n\\n\\n\\n\\nWe'll come back later to this interface, for the proxy configuration for exampleIt's the next part\\n\\n\\n\\nAdd a proxy and a web filter\\n\\n\\n\\nWhat's a proxy?\\n\\n\\n\\nA proxy has three main roles:\\n\\n\\n\\nCreating a cache of all Internet pages, to increase web browsing speedLog all pages, to generate reports (top domain, top traffic, ...)And we can add a website blocker, to deny access to some kinds of content\\n\\n\\n\\nTo do this, we'll install Squid (the proxy) and SquidGuard (the filter) on the Raspberry Pi\\n\\n\\n\\nSquid installation\\n\\n\\n\\nSquid is available in the repository. Install it with: sudo apt install squid Backup the configuration file:cd \\/etc\\/squid sudo mv squid.conf squid.conf.old Switch to the root user a few seconds and remove all the comments quickly sudo su cat squid.conf.old | egrep -v -e '^\[\[:blank:\]\]\*#' | grep \\"\\\\S\\" &gt; squid.confexitThen edit the configuration file:sudo nano squid.conf And add these lines at the beginning acl LocalNet src 192.168.42.0\\/24 http\_access allow LocalNet Squid works only on HTTP for the Wi-Fi network (42.X) Restart Squid to apply changes sudo systemctl restart squid \\n\\n\\n\\nOnce Squid is configured, you have two choices to use it:\\n\\n\\n\\nConfigure your web browser to use the Raspberry Pi as the HTTP ProxyIt depends on your browser, but you should&nbsp;find this option in Options &gt; Network settingsConfigure iptables to redirect automatically all HTTP traffic to squidIt should be something like this: &nbsp; iptables -t nat -A PREROUTING -i wlan0 -p tcp --dport 80 -j DNAT --to 192.168.42.1:3128 iptables -t nat -A PREROUTING -i eth0 -p tcp --dport 80 -j REDIRECT --to-port 3128 \\n\\n\\n\\nThen check that HTTP websites are working fineYou can see all the websites visited in the Squid log file&nbsp;:\\n\\n\\n\\nsudo tail -f \\/var\\/log\\/squid\\/access.log\\n\\n\\n\\nWebmin add-on\\n\\n\\n\\nThere is a Webmin add-on called \\"calamaris\\" you can install to monitor the proxy efficiencyInstall it with apt:\\n\\n\\n\\nsudo apt install calamaris\\n\\n\\n\\nAnd then go back to webmin, in the unused modules to find new tools for squid monitoring\\n\\n\\n\\nSquidGuard installation\\n\\n\\n\\nWe can now move to the SquidGuard installation:\\n\\n\\n\\nInstall the squidguard package sudo apt install squidguard Download a list of websites by category wget http:\\/\\/squidguard.mesd.k12.or.us\\/blacklists.tgz Extract files from the archive tar -zxvf blacklists.tgz While extracting, you'll see some&nbsp;blacklist categories appear on your screenYou can choose one and use it for the SquidGuard configuration laterYou can open the files to get some&nbsp;websites examples Move files to the SquidGuard folder sudo mv blacklists \\/var\\/lib\\/squidguard\\/db Archive the original SquidGuard configuration file cd \\/etc\\/squiguard mv squidGuard.conf squidGuard.conf.old Create a new configuration file sudo nano squidGuard.conf Paste these lines dbhome \\/var\\/lib\\/squidguard\\/db logdir \\/var\\/log\\/squidguard dest violence { domainlist blacklists\\/violence\\/domains urllist blacklists\\/violence\\/urls log violenceaccess } acl { default { pass&nbsp;!violence redirect http:\\/\\/localhost\\/block.html } } This is a sample file, you can block whatever you wantYou can also add more categories by creating more dest sections Save and exit (CTRL+O, CTRL+X)Build the SquidGuard database sudo squidGuard -C all -d This can take a long time. If it's too long, remove files you don't need from the blacklists folderUse a screen if you don't stay in front of your computer (screen -S build)So if the SSH connection with your computer is lost, this will not stop the build process Restart Squid to apply changes sudo service squid restart \\n\\n\\n\\nIt should be ok now, try to access a URL from the domain list and check that&nbsp;you are blocked by squidGuard\\n\\n\\n\\nRelated questions\\n\\n\\n\\nIs it possible to add an Ad Blocker brick in this router? Yes, you can use Pi-Hole to do this, it's easy to install and you just&nbsp;need to set the Raspberry Pi as your DNS server (manually or in the DHCP configuration file, see Firewall &gt; DNS issues for more information)\\n\\n\\n\\nIs it possible to use a Raspberry to build a \\"full Ethernet\\" router? Yes, you can add an Ethernet hat to your Raspberry Pi like this expansion Hat (more details on Amazon). It's perfect for a firewall.\\n\\n\\n\\nConclusion\\n\\n\\n\\nThat's it, you should&nbsp;now have better knowledge on how to build a complete firewall router with proxy on a Raspberry Pi\\n\\n\\n\\nI hope it's working for you.It took me a lot of time to write this post with many tests I didn't include here, but you have the most important things, with the best toolsIf you have any issues, ask your question in the community, we'll try to help you\\n\\n\\n\\nAlso, these tools are basically Linux stuff and you can find a lot of help on the Internet to go further\\n\\n\\n\\nI give you all the documentation links here if needed:\\n\\n\\n\\nRPI Wifi routerIptablesSquidSquidGuardPi Hole","headline":"How to use Raspberry Pi as a Wireless Router with Firewall?","author":{"@type":"Person","name":"Patrick Fromaget","url":""},"datePublished":false,"mainEntityOfPage":"True","dateModified":false,"image":{"@type":"ImageObject","url":"https:\\/\\/raspberrytips.com\\/wp-content\\/uploads\\/2020\\/06\\/install-firewall-router-wifi-raspberry-pi-1024x683.jpg","height":427,"width":640},"publisher":{"@context":"http:\\/\\/schema.org\\/","@type":"Organization","name":"Raspberry tips","logo":{"@type":"ImageObject","url":"https:\\/\\/raspberrytips.com\\/wp-content\\/uploads\\/2020\\/08\\/RaspberryTips-300x150.png","height":600,"width":60}}}

[

](https://raspberrytips.com/author/admin/)

[Patrick Fromaget](https://raspberrytips.com/author/admin/)

I'm the lead author and owner of RaspberryTips.com. My goal is to help you with your Raspberry Pi problems using detailed guides and tutorials. In real life, I'm a Linux system administrator with a web developer experience.

### Recent Posts

[

link to What is the SSH password for Raspberry Pi?](https://raspberrytips.com/ssh-password-raspberry-pi/)

[What is the SSH password for Raspberry Pi?](https://raspberrytips.com/ssh-password-raspberry-pi/)

If you want to access your Raspberry Pi from a remote computer, you can use SSH and get a terminal as if you were on the Raspberry Pi directly. But, you'll need the IP address and the SSH password in...

[Continue Reading](https://raspberrytips.com/ssh-password-raspberry-pi/)

[

link to How To Connect Ubuntu To Your Wi-Fi (Desktop & Server)](https://raspberrytips.com/connect-wi-fi-ubuntu/)

[How To Connect Ubuntu To Your Wi-Fi (Desktop & Server)](https://raspberrytips.com/connect-wi-fi-ubuntu/)

Ubuntu is a great Linux distribution for beginners, with most things being intuitive enough to get started quickly. It doesn't mean that everything is easy. One of the first steps will be to connect...

[Continue Reading](https://raspberrytips.com/connect-wi-fi-ubuntu/)

Welcome
-------

![Site logo](https://raspberrytips.com/wp-content/uploads/2018/07/RaspberryTipsLogo80.png)

  

Hi, I'm Patrick. I am a Linux system administrator, and I am passionate about the Raspberry Pi and all projects on this topic.  
I created this site to share with you what I learned about it.  
  

[About Page](https://raspberrytips.com/about)

My Commands Cheat Sheet
-----------------------

[![My Commands Cheat Sheet](https://raspberrytips.com/wp-content/uploads/2021/08/commands-cheatsheet.png)](https://raspberrytips.com/sb-commands)

  
Grab your free PDF file with all the commands you need to know on Raspberry Pi!  
  

[Free Download](https://raspberrytips.com/sb-commands)

Join the community
------------------

*   Chat with other Raspberry Pi users
*   Ask for advices
*   Get access to exclusive content
*   Browse the website without ads
*   and more...

[Join now!](https://raspberrytips.com/community)

*   [Home](https://raspberrytips.com)
*   [Master your Raspberry Pi (eBook)](https://raspberrytips.com/tm-ebook)
*   [Beginner Course](https://raspberrytips.com/tm-course)
*   [Master Python on Raspberry Pi](https://raspberrytips.com/masterpython-tm)
*   [Resources](https://raspberrytips.com/resources/)
*   [Write for Us](https://raspberrytips.com/contribute/)
*   [Contact](https://raspberrytips.com/contact/)
*   [Affiliate Program](https://raspberrytips.com/affiliate-program/)
*   [Privacy Policy](https://raspberrytips.com/privacy-policy/)
*   [About Me](https://raspberrytips.com/about-patrick-fromaget/)
*   [About RaspberryTips](https://raspberrytips.com/about/)
*   [Terms and Conditions](https://raspberrytips.com/terms-and-conditions/)
*   [Version Française](https://raspberrytips.fr)
*   [Versión española](https://raspberrytips.es)

Copyright © 2022 RaspberryTips. All rights reserved.

[Join the community!](https://raspberrytips.com/community)

This site is owned and operated by Patrick Fromaget. RaspberryTips.com is a participant in the Amazon Services LLC Associates Program, an affiliate advertising program designed to provide a means for sites to earn advertising fees by advertising and linking to Amazon.com. This site also participates in other affiliate programs and is compensated for referring traffic and business to these companies.  
Raspberry Pi is a trademark of the Raspberry Pi Foundation

jQuery("#post-1341 .entry-meta .date").css("display","none"); jQuery("#post-1341 .entry-date").css("display","none"); jQuery("#post-1341 .posted-on").css("display","none"); window.llvConfig=window.llvConfig||{};window.llvConfig.youtube={"colour":"red","buttonstyle":"","controls":true,"loadpolicy":true,"thumbnailquality":"0","preroll":"","postroll":"","overlaytext":"","loadthumbnail":true,"cookies":false,"callback":"<!--YOUTUBE\_CALLBACK-->"}; window.llvConfig=window.llvConfig||{};window.llvConfig.vimeo={"buttonstyle":"","playercolour":"","preroll":"","postroll":"","show\_title":false,"overlaytext":"","loadthumbnail":true,"thumbnailquality":false,"callback":"<!--VIMEO\_CALLBACK-->"}; jQuery("a\[href\*='amazon.com'\]").each(function(){ this.href = this.href.replace(/aax-us-east.amazon-adsystem.com\\/x\\/c\\/\[a-z ^a-z ^A-Z A-Z ^0-9 0-9\_-\]+\\/https/g, ''); this.href = this.href.replace(/amazon\\.com\\/\[a-z ^a-z ^A-Z A-Z ^0-9 0-9\_-\]+\\/dp\\//g, 'amazon.com/dp/'); this.href = this.href.replace(/amazon\\.com\\/\[a-z ^a-z ^A-Z A-Z ^0-9 0-9\_-\]+\\/b\\//g, 'amazon.com/b/'); this.href = this.href.replace(/\\?ref=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/ref=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\?ref=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\?s=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\&qid=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\&sr=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\+/g, ''); this.href = this.href.replace(/\\&keywords=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\?\_encoding=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\&psc=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\?pf\_rd\_m=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\&pf\_rd\_r=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\&pf\_rd\_t=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\&pf\_rd\_p=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\&pf\_rd\_i=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\&heroAsin=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\&source=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\&pf\_rd\_m=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\?smid=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\/ref\_%\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\?tag=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\&pf\_rd\_s=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\?creativeASIN=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\&linkCode=\[a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\&imprToken=\[.a-z A-Z 0-9\_-\]+/g, ''); this.href = this.href.replace(/\\&slotNum=\[a-z A-Z 0-9\_-\]+/g, ''); }); var amzid = 'rpitips-20' jQuery("a\[href\*='amazon.com'\]").each(function(){ this.href += "?tag="+amzid; });

//Patreon jQuery(function() { jQuery(".wpd-blog-subscriber .wpd-comment-author").prepend("<a href='https://patreon.com/raspberrytips' target='\_blank'><img src='https://raspberrytips.com/wp-content/uploads/2022/04/patreon-icon.png' width='16px'/></a>"); jQuery(".wpd-blog-subscriber .wpd-comment-header").append("<div class='wpd-comment-label' wpd-tooltip='Patron' wpd-tooltip-position='top' style='background-color:#ff5600'><span>Patron</span></div>"); })

\_\_ez.queue.addFile('/detroitchicago/edmonton.webp', '/detroitchicago/edmonton.webp?a=a&cb=18&shcb=34', true, \['/detroitchicago/minneapolis.js'\], true, false, false, false); \_\_ez.queue.addFile('/porpoiseant/jellyfish.webp', '/porpoiseant/jellyfish.webp?a=a&cb=18&shcb=34', false, \[\], true, false, false, false); \_\_ez.queue.addFile('/tardisrocinante/vitals.js', '/tardisrocinante/vitals.js?gcb=18&cb=3', false, \['/detroitchicago/minneapolis.js'\], true, false, true, false); var \_audins\_dom="raspberrytips\_com",\_audins\_did=97361;\_\_ez.queue.addDelayFunc("audins.js","\_\_ez.script.add", "//go.ezoic.net/detroitchicago/audins.js?cb=195-18");

![Quantcast](//pixel.quantserve.com/pixel/p-31iz6hfFutd16.gif?labels=Domain.raspberrytips_com,DomainId.97361)

\_\_ez.queue.addFile('/beardeddragon/drake.js', '/beardeddragon/drake.js?gcb=18&cb=4', false, \[\], true, false, true, false); \_\_ez.queue.addFile('/beardeddragon/tortoise.js', '/beardeddragon/tortoise.js?gcb=18&cb=4', false, \[\], true, false, true, false); let ezVideoIframe=false;function renderEzoicVideoContent(){let videoObjects=\[{"PlayerId":"ez-2","VideoContentId":"75a14af930054b1f02d62d8dbddd9efc6f75852c55bb0095a82036e505690e28","VideoPlaylistSelectionId":0,"VideoPlaylistId":0,"VideoTitle":"pfSense VMWare ESXi Installation and Basic Wizard Configuration","VideoDescription":"I recorded this video to present how easy to set up an open source firewall at your home network. I used pfSense as an example, but there are some others can be found from Internet such as , OPNsense, IPFire, Smoothwall. \\n\\nThis video shows the installation process on VMWare ESXi, but it is same process on Workstation or other virtual environment.\\nSteps:\\n1. Download Image\\n2. Create VM and boot it from download ISO image\\n3. Log into Web GUI from LAN network\\n4. After log into system, complete Wizard for basic configuration. After this step done, your LAN network machines should be able to reach WAN or Internet.\\n5. Create some additional firewall rules.\\n\\nPfsense Video in my channel:\\n1.pfSense VMWare ESXi Installation and Basic Wizard Configuration: https://youtu.be/c1vI1L-TSLA\\n2. Pfsense Home Configuration with Recommended Package Installation: https://youtu.be/BabQh2d1tPU\\n\\nSubscribe me: https://www.youtube.com/c/Netsec?sub\_confirmation=1\\n\\n\\n=======================================================\\nRecording IT life Blog: https://51sec.org","VideoLinksSrc":"https://streaming.ezoic.com/link/75a14af930054b1f02d62d8dbddd9efc6f75852c55bb0095a82036e505690e28.vtt","Captions":null,"VideoDurationMs":797196,"DeviceTypeFlag":0,"FloatFlag":1,"FloatOptionFlag":1,"IsAutoPlay":true,"IsLoop":false,"ShouldConsiderDocVisibility":false,"ShouldPauseAds":false,"AdUnit":"","ImpressionId":0,"VideoStartTime":0,"IsStartTimeEnabled":0,"IsKeyMoment":false,"PublisherVideoContentShare":{"DomainIdOwner":124125,"DomainIdShare":97361,"DomainNameOwner":"51sec.org","IsEzoicOwnedVideo":false,"IsOutstream":false},"VideoUploadSource":"","VAbTest":"vmod2","VAbTestVal":"","VideoPlaylist":null,"VideoPlaceholderId":2,"URL":"https://raspberrytips.com/raspberry-pi-firewall/","Width":640,"MaxWidth":"","Height":360,"PreviewURL":"https://raspberrytips.com/ezoimgfmt/video-streaming.ezoic.com/poster/HvEzanNctrNCjLBl/75a14af930054b1f02d62d8dbddd9efc6f75852c55bb0095a82036e505690e28\_pOHKFz.jpg?ezimgfmt=ng%3Awebp%2Fngcb1%2Frs%3Adevice%2Frscb1-2","VideoDisplayType":1,"MatchOption":0,"PlaceholderSelectionId":0,"HashValue":"","IsFloating":true,"AdsEnabled":0,"IsAutoSelect":true,"Keyword":"","VideoSelection":2,"VideoMatchScore":74,"VideoPlaceholderHash":"","IsAIPlaceholder":false}\];if(typeof ezVideoPlayer==="undefined"){\_\_ez.queue.addFile("/beardeddragon/wyvern.js",'/beardeddragon/wyvern.js?cb=46',true,\[\],false,true,true,false);\_\_ez.queue.addFile("/beardeddragon/gilamonster.js",'/beardeddragon/gilamonster.js?cb=112',true,\["/beardeddragon/wyvern.js"\],false,true,true,false);\_\_ez.queue.addFile("/beardeddragon/gecko.js",'/beardeddragon/gecko.js?cb=32',true,\[\],false,true,true,false);\_\_ez.queue.addFile("/beardeddragon/iguana.js",'/beardeddragon/iguana.js?cb=122',true,\["/beardeddragon/wyvern.js","/beardeddragon/gecko.js"\],false,true,true,false);\_\_ez.queue.addFunc("ezoicVideoNonCmb","renderEzoicVideoContent",null,false,\["/beardeddragon/iguana.js"\],false,false,true,false);return;} window.ezIntType="";for(vIndex=0;vIndex<videoObjects.length;vIndex++){let videoObject=videoObjects\[vIndex\];videoObject.videoObjectsCount=videoObjects.length;videoObject.videoObjectsIndex=vIndex+1;ezVideoPlayer.Init(videoObject);}} \_\_ez.queue.addFile("/beardeddragon/wyvern.js",'/beardeddragon/wyvern.js?cb=46',true,\[\],false,true,true,false);\_\_ez.queue.addFile("/beardeddragon/gilamonster.js",'/beardeddragon/gilamonster.js?cb=112',true,\["/beardeddragon/wyvern.js","/porpoiseant/jellyfish.webp"\],false,true,true,false);\_\_ez.queue.addFile("/beardeddragon/iguana.js",'/beardeddragon/iguana.js?cb=122',true,\["/beardeddragon/gilamonster.js","/beardeddragon/gilamonster.js"\],false,true,true,false);\_\_ez.queue.addFunc("ezoicVideo","renderEzoicVideoContent",null,false,\["/beardeddragon/iguana.js"\],false,false,true,false);