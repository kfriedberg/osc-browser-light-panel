# UDP -> Web Socket Light Panel

This is a modification of an example which illustrates a Node.js server that will relay OSC messages sent via
a UDP socket (listening on port 57121) to a web page using a Web Socket connection.

By default, it is configured to handle OSC messages via UDP from Isadora's OSC Multi Transmit actor.
It maps three parameters from Isadora's actor to the RGB values of the background colour of the browser page.

This project is forked from the browser osc.js example, found at https://github.com/colinbdclark/osc.js-examples/tree/master/browser

## Installation

1. From the internet, download and unpack/install the node.js server
2. Place this project at the root of the server
3. Run <code>npm install</code> in the terminal to install all required Node dependencies
4. In the <code>web</code> directory, run <code>..\npm install</code> to install all web dependencies

## Running the Example

1. Run <code>node .</code> in the Terminal
2. Open <code>http://thisserversaddress:8081/?address=/oscaddress</code> (choose your own <code>oscaddress</code>) in your browser
3. Control the page colour using OSC messages sent from Isadora or another OSC server to <code>thisserveraddress</code>, port <code>57121</code>, address <code>/oscaddress</code>

## Troubleshooting
<code>Error: bind EACCES 0.0.0.0:57121</code>
Open a command prompt as admin and run <code>net stop winnat</code> followed by <code>net start winnat</code>