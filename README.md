## umres libs
the web front-end resource cdn

### nginx config
~~~
location ~ .*\.(js|css|png|jpg|jpeg|gif|bmp|ico|eot|ttf|woff|woff2|svg|svgz)$
{
    expires 365d;
    access_log off; 
}

location ~ ^(.*)/$ 
{
	autoindex on;
    #autoindex_localtime on;
    #autoindex_exact_size off;
    add_before_body /umres-libs/header.min.html; 
}
~~~