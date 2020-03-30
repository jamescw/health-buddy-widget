#health-buddy-widget

Copy the content of index.html into your project.
Please make sure that `bot.js` and `chat.css`, as well as the image assets are being referenced correctly.
```
<link href="assets/css/chat.css" rel="stylesheet">
<script src="assets/js/bot.js"></script>
<div id="webchat"/>
  <script>
  function isMobile() {
  try{ document.createEvent("TouchEvent"); return true; }
  catch(e){ return false; }
}
    var userLang = 'en';
    console.log(userLang)
    var initPayload = 'hello ' + userLang;
    if(!isMobile()) {
      WebChat.default.init({
    		selector: '#webchat',
    		initPayload: initPayload,
    		channelUuid: 'f2cc9ec6-07f1-407a-8948-ece57761d88e',
    		host: 'https://rapidpro.ilhasoft.mobi',
    		title: 'HealthBuddy',
        hideWhenNotConnected: false,
    		inputTextFieldHint: "Type a question...",
    		profileAvatar: './assets/img/doctor-darker.png',
    		openLauncherImage: './assets/img/doctor-square.png',
        disableTooltips: true,
    		docViewer: true,
    		showFullScreenButton: true,
        hideWhenNotConnected: true,
      	params: {
    			images: {
    				dims: {
    					width: 712,
    					height: 844
    	          	}
    			},
    			storage: "session"
    		}
        });
    } else {
      WebChat.default.init({
    		selector: '#webchat',
    		initPayload: initPayload,
        tooltipPayload: initPayload,
    		channelUuid: 'f2cc9ec6-07f1-407a-8948-ece57761d88e',
    		host: 'https://rapidpro.ilhasoft.mobi',
    		title: 'HealthBuddy',
        hideWhenNotConnected: false,
    		inputTextFieldHint: "Type a question...",
        profileAvatar: './assets/img/doctor-darker.png',
        openLauncherImage: './assets/img/doctor-square.png',
        disableTooltips: false,
    		docViewer: true,
    		showFullScreenButton: true,
        hideWhenNotConnected: true,
    		params: {
    			images: {
    				dims: {
    					width: 712,
    					height: 844
    	          	}
    			},
    			storage: "session"
    		}
        });
    }

  </script>
```