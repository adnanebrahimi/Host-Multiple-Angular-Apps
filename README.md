# Host-Multiple-Angular-Apps
An example of how to config .htaccess files


We faced with projects that have more than one angular apps in their sub folders. This is my experince to how to handle this kind of .htaccess configuration:


    Domain.com/app_1/
               app_2/
               app_../
               app_N/
           
           
           
           
       
## Root folder (/)
       
       RewriteRule ^app_1/. /app_1/index.html [NC,L]
       RewriteRule ^app_2/. /app_2/index.html [NC,L]
           

       
## Sub folders (/app_1)
       
        RewriteRule ^ /app_1/index.html [NC,L]

## Sub folders (/app_2)
       
        RewriteRule ^ /app_2/index.html [NC,L]
           
