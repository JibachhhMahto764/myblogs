---
title: "What are cookies, and how do they work?"
datePublished: Fri Dec 22 2023 04:01:28 GMT+0000 (Coordinated Universal Time)
cuid: clqg3u3ki000808jq7geh5izn
slug: what-are-cookies-and-how-do-they-work
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1703214701935/9c433821-91cf-49c4-ae89-6f1eb8de2c60.png
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1703217639106/6ccefd16-7460-41d4-85ab-e9654b028b41.png
tags: cookies, web-development, session

---

Basically a cookies are often used to identify a user. A cookie is a small file that the server embeds on the users computer. Each time the same computer requests a page with a browser. it will send the cookie too. website that collects cookies will typically work as follows:

1. **A user logs on to a website for the first time.**
    
2. **The website assigns that user an ID and stores the information in its database.**
    
3. **The ID that is created is sent to the browser, which saves the ID on the computer’s hard drive.**
    
4. **The next time that user visits the website, the ID stored on their computer is looked up in the database and the website, and they do not have to log in again.**
    

So the sole purpose of most cookies is to add convenience to websites you frequently visit — specifically, storing logins, remembering preferences, recognizing you as a subscriber for subscription-only content, and so on.

**HOW GOOGLE USES COOKIES**

%[https://youtu.be/TBR-xtJVq7E] 

## Create a cookie with PHP

A Cookie is created with the setcookie() function.

syntax:-

setcookie(name,value,expire,domain,secure,httponly);

### creating and retrieving a cookie

```php
<?php
$cookie_name = "user";
$cookie_value = "JIbachh singh";
setcookie($cookie_name, $cookie_value, time() + (86400*30),"/";
if(!isset($_COOKIE[$cooki_name])){
echo "Cookie named ' ". $cookie_name . " ' is not set";
}
else{
echo " Cookie ' " . $cooki_name . " ' is set! <br>";
echo "Value is : " . $_COOKIE[$cookie_name];
}
?>
```

### How to Delete Cookie.?

To delete a cookie use the setcookie() function with an expiration date in the past.

```php
<?php
// set the expiration date to one hour ago
setcookie("user" , "", time() - 3600);
echo" cookie 'user' is deleted. ";
?>
```

## what is a Session?

When you work with an application, you open it, make some changes and then you close it. this is much like a session. Session basically means that holds information about one single user and is available to all pages in one application.

### Starting PHP Session.?

A PHP session is easily started by making a call to the session\_start() function. This function first checks if a session is already started and if none is started then it starts one, It is recommended to put the call to session *start() at the beginning of the page. Session variables are stored in an associative array called $*\_SESSION\[\]. These variables can be accessed during the lifetime of a session.

```php
<?php
// start the session 
session_start();
// set session variables
$_SESSION["username"] = " jibachh";
$_SESSION["email"] = " jibachh@gmail.com";
echo " Session variables are set.";
?>
```

### How to destroy a PHP Session.

To remove all global session variables and destroy the session, use session\_unset() and session\_destroy()

```php
<?php
session_start();
?>
// remove all session variables 
session_unset();
// destroy the session 
session_destroy();
?>
```