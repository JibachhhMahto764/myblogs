---
title: "How we access the internet    /"
datePublished: Mon Dec 18 2023 15:46:43 GMT+0000 (Coordinated Universal Time)
cuid: clqb39n7z000h09lhbtd50wx6
slug: how-we-access-the-internet
tags: web-development, webdev

---

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1702914303666/bff2e560-d5c9-4b56-abeb-7fbc110b2aa0.png align="center")

The first connection your computer makes when getting on the internet is to your [LAN, or Local Area Connection](https://www.howtogeek.com/353283/what-is-a-local-area-network-lan/). A LAN is a single network that multiple devices can access in a single location. The obvious example is your modem at home that provides an internet connection and its router (most likely [Wifi](https://www.cisco.com/c/en/us/products/wireless/what-is-wifi.html#:~:text=Wi%2DFi%20is%20a%20wireless,to%20interface%20with%20the%20Internet.&text=Internet%20connectivity%20occurs%20through%20a%20wireless%20router.)) that allows multiple devices like your phone, computer, and TV to share the same connection. Your LAN then connects to an even larger network known as a [WAN, or Wide Area Network](https://www.cisco.com/c/en/us/products/switches/what-is-a-wan-wide-area-network.html). The WAN is a collection of LANs and is most likely a router run by your [ISP or Internet Service Provider](https://en.wikipedia.org/wiki/Internet_service_provider). Your immediate WAN is probably located in your neighborhood, which is then connected to another regional WAN, perhaps for your entire city or town. This cycle is repeated, and after multiple “[hops](https://www.lifewire.com/what-are-hops-hop-counts-2625905)”, you are connected to the “[backbone](https://www.networkworld.com/article/3532318/what-is-the-internet-backbone-and-how-it-works.html)” of the internet.

## **Domain Name System (DNS)**

When you navigated to the URL for this article, your browser (aka the client) first needed to conduct a [DNS or Domain Name System](https://www.keycdn.com/support/what-is-a-dns-server) lookup. The DNS is like the phonebook of the internet. Every website has a unique [IP address](https://en.wikipedia.org/wiki/IP_address) that can be found in the DNS via the website’s domain name. Your browser first checks your own device’s locally cached DNS storage to see if it has looked up the domain name before and has the IP address. If not found, it checks your Internet Service Provider’s DNS records, where the IP address can usually be resolved. The IP address will then be cached locally on your machine for a quicker lookup next time. This IP address will be used for the HTTP request.

## **HTTP Request**

An [HTTP request](https://www.codecademy.com/articles/http-requests) with the IP Address is then sent to the corresponding server. All HTTP requests and responses use [Transmission Control Protocol (TCP)](https://www.fortinet.com/resources/cyberglossary/tcp-ip). TCP is one of the most basic standards of the internet that ensures end-to-end communication and the delivery of data. So your request opened a TCP channel to the server that is hosting the requested data that is located via the URL’s IP address. The server then approved the request and sent back a “200 OK” [HTTP status message](https://www.w3schools.com/tags/ref_httpmessages.asp). The 200 code tells your browser that your request was properly received and that data is being sent your way.

The transfer of data is made possible by the internet, not the web —remember, the internet is the *infrastructure*. Each data packet must conform to a standard known as [Internet Protocol (IP)](https://en.wikipedia.org/wiki/Internet_Protocol). Similar to how packages are actually sent through the mail, each packet of data must have the [IP Address](https://en.wikipedia.org/wiki/IP_address) of where it’s going and also must abide by a regulated size limit. In your case, the packets had your computer’s IP address on them. If the data packets (aka files) are large, they are split into smaller packets and sent through many channels with different hops, then reassembled when they reach the client (your computer).

## **More on “hops”**

A request might take 2 hops to get onto the backbone of the internet, 2 hops on the backbone, and then 3 hops down to hit the server. The data packet sent back would then possibly be split into smaller packets, all taking multiple hops to get to the backbone, then multiple hops to get off the backbone, and down to your local machine, where they are all reassembled into one file or packet.

You can actually view all the hops your request data is taking by using “[Traceroute](https://en.wikipedia.org/wiki/Traceroute)” — see directions for Mac [here](https://www.godaddy.com/help/performing-a-traceroute-in-mac-os-x-3366), directions for Windows [here](https://www.hellotech.com/guide/for/how-to-run-a-traceroute-windows-10), and Linux [here](https://www.howtogeek.com/657780/how-to-use-the-traceroute-command-on-linux/).

## **Parsing the website**

Our request for the website has returned an [HTML](https://www.w3schools.com/html/html_intro.asp) file, which is parsed by our browser. The HTML contains links to the [CSS](https://www.w3schools.com/css/css_intro.asp) and [JavaScript](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/First_steps/What_is_JavaScript) that will be referenced for the site. After the HTML is parsed and the [DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction) has been constructed, the CSS is applied and the first visual representation of the website is “painted” in our browser. Finally, the JavaScript is parsed and applied to make the site interactive.