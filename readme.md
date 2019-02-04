Firstly, If you get an error like "cURL error 60: SSL certificate problem: unable to get local issuer certificate".

Solution:
- You should download file:
https://curl.haxx.se/docs/caextract.html  and put it here:

*For XAMPP SERVER
    "C:\xampp\php\e"xtras\ssl\cacert.pem"
in your php.ini put this line in this section (“c:\xampp\php\php.ini”);

*For WAMP SERVER
    "C:\wamp64\bin\php\phpX.X.X\extras\ssl\cacert.pem" 
in your php.ini put this line in this section (“C:\wamp64\bin\php\phpX.X.X\php.ini”);

*In php.ini

<code class="hljs"><span class="pun">;;;;;;;;;;;;;;;;;;;;</span>
<span class="pun">;</span><span class="pln"> php</span><span class="pun">.</span><span class="pln">ini </span><span class="typ">Options</span>  <span class="pun">;</span>
<span class="pun">;;;;;;;;;;;;;;;;;;;;</span><span class="pln">

curl</span><span class="pun">.</span><span class="pln">cainfo </span><span class="pun">=</span> <span class="str"><span class="hljs-string">"C:\xampp\php\extras\ssl\cacert.pem"</span></span></code>

Finally, restart your server.
