# Problems
I was using a blurred background for the slider but the problem was that it was very laggy so I had to remove them.

I had a problem linking styles together so I had to use event listener code I found on stackoverflow in order to start a new animation at the end of another.

When I first used ajax to load the webpage I tried updating the background content but when I did that it interrupted it. Adding the load() function inside the event listener fixed that.

When I try and to set the contents of a div (qrcode) to none it gives this error `_slide.js:59 Uncaught TypeError: Cannot set property 'innerHTML' of null`. This is not really a problem though since its only happens the first time the function is called and doesn't cause issues every time after that since the html has fully loaded at that point. This error doesn't crash the program it just continues. I could add error correction for completeness.

When I started doing the transitions I used js and html but my code started getting messy and it wasn't obvious where actions were being called from so I decided to use jquery. I will be able to organise them better in folders which will help me maintain the project.

Currently my website allows buttons to be clicked even thought the cursor has a 'not-allowed' icon appear over the button so I am going to have to add validation in the jquery to check that the button should be clickable.

I have started implementing the private keys on my application and originally I thought the only library I would need it bitcoinjs-lib but I actually needed a library names bip39 because that library is not included in bitcoinjs-lib. I used browserify in order to make both libraries work in the browser.

I am having issues with auto-updating the amount in the users wallet because I don't want to spam API's so I have to send a http request every 60 seconds or so which isn't responsive enough from the users point of view. I will probably have to download the blockchain on a server and use socket.io to get realtime data.

https://github.com/bitcoinjs/bitcoinjs-lib/issues/1052

I was having issues retriving the state of the blockchain and I could do it locally on my own computer but that requires running an indepentant peice of software with a storage requirement in the hundreds of gigabytes so in order to make it more lightweight I'm going to use an API. Blockcypher.


I had enough issues getting sending and receiving to work for Bitcoin never mind Litecoin. In order to simplify the swapping of cryptocurrency I am going to use a third-party service which I was reluctant to do but decentralised alternatives are not ready for production. I will use Shapeshift since they are a well established service and have the best prices with the smallest fees. Someone has already went to the work of making an library that I can use in npm so that what i'll be using for this.
