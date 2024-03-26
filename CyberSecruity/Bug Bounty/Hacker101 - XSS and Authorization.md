Notes on the video [Hacker101](https://www.youtube.com/watch?v=HGaFCcWM57U&list=PLxhvVyxYRviZd1oEA9nmnilY3PhVrt4nj&index=3)
# XSS Review

Three types of XSS that is going to be covered today:
	Reflected XSS - Input from a user is directly returned to the browser, permitting injection of arbitrary content 
	Stored XSS - Input from a user is stored on the server and returned later without proper escaping
	DOM XSS - Input from a user is inserted into the page's DOM without proper handling, enabling insertion of arbitrary nodes
Recognition 
	Should follow a mental checklist for each input 
	1. Figure out where it goes: Does it get embedded in a tag attribute? Does it get embedded into a string in a script tag?
	2. Figure out any special handling: Do URLs get turned into links like posts in level1?
	3. Figure out how any special characters are handled: A good way is to input something like '<>;:''
	From those