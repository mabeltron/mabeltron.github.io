---
Title: Host based redirects in nginx
Date: 2016-11-08 07:57:13
Category: Hints and Tips
Tags: nginx, redirects
layout: post
---
I work with a server that we inherited from a managed server company who set their systems up with a fairly standard web serving architecture of [nginx][f11e5976] in front and [Apache httpd][1b8f3839] serving [PHP][aa77cd72] at the back. What is slightly odd is that in Nginx the hosts are all in a map to a docroot which is then served from a default server like this:

```
map $host_name $docroot {
    domain1.com /home/user/domain1.com/public_html;
    domain2.com /home/user/domain2.com/public_html;
    ...
    default /dev/null;
}
```

 This makes for easy configuration if all you are doing is serving over HTTP, but the client wanted to start using HTTPS. Easy enough in the first case: create a server configuration in nginx that listens on an IP address on port 443 and enable ssh and all is fine. However, enforcing HTTPS is something else. Usually it's a just a redirect, but that is based on the server name and if you don't specify a server name, then all domains get forwarded to the SSL enabled domain. Oops.

It took a bit of thinking but the answer is another map and a conditional declaration. The developers of nginx [consider 'if' to be evil][0cf43213] mostly because its engine is imperfect and could return unexpected results up to a segfault, not to mention that you would end up with a lot of ifs in a large installation like this. So a map like this:

```
map $host_name $to_https {
    domain1.com 1;
    domain2.com 1;
    default 0;
}
```

and a conditional statement in your main server configuration:

```
if ($to_https = 1) {
    return 301 https://$to_https$1
}
```

creates a slightly unconventional but functional way of enforcing HTTPS.

  [f11e5976]: https://nginx.org "Nginx"
  [1b8f3839]: https://httpd.apache.org "Apache httpd"
  [aa77cd72]: https://php.net "PHP"
  [0cf43213]: https://www.nginx.com/resources/wiki/start/topics/depth/ifisevil/ "If is Evil"
