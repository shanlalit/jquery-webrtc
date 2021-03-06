# Plugin jQuery - webRTC

This plugin is a part of a project developed by Clément Mouret and Luc Tribolet during an internship at Atos Worldline.

It is only available for Chrome/Chromium with support WebRTC. This web application includes a jQuery plugin for the webRTC and allows you to video chat with someone else by sharing a single link. 

## Requirements

You have to install 

- a signaling server for webRTC (You can get the code source on GitHub : https://github.com/MouMou/EWP)
- a HTTP server
- Chrome or Chromium (please get the latest version of Chrome/Chromium Dev or Chrome Canary to avoid troubles and issues)

## Installation

1. Get the sources
2. Move them in your www directory
3. Complete the plugin options in index.php
4. Launch your signaling server for webRTC
5. Open the page http://yourserver/
6. Enjoy

## Configuration

Place a div element in your page with an id attribute (i.e &lt;div id="#conversation"&gt;&lt;/div&gt;)

Create a webrtc object like this : 

	$('#conversation').createWebrtc(); 

And that's it.

You can configure though several options :

	$('#conversation').createWebrtc({
    	local: '#customLocalVideo',
    	remote: '#customRemoteVideo',
    	status: '#customStatus',
    	signallingServer: 'ws://yourserver:port',
		serverStunTurn: 'addressofyourserver',
		urlParameters : 'room',
		mediaParametersAudio: true,
		mediaParametersVideo: true
    });



# Credits

This project use the differents following projects :

- jQuery
- Bootstrap Twitter

And it's been inspired directly from this application : https://apprtc.appspot.com/