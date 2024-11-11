## مراحل نصب

### مرزبان

۱. **قالب رو با دستور زیر دانلود کنید**
   ```sh
   sudo wget -N -P /var/lib/marzban/templates/subscription/ https://github.com/MR-MKZ/template-loader/releases/download/v1.0.0/index.html
   ```

۲. **دستورات زیر رو تو ترمینال سرورتون بزنید**
   ```sh
   echo 'CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"' | sudo tee -a /opt/marzban/.env
   echo 'SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"' | sudo tee -a /opt/marzban/.env
   ```
   یا مقادیر زیر رو در فایل `.env` در پوشه `/opt/marzban` با پاک کردن `#` اول آنها از حالت کامنت در بیارید.
   ```
   CUSTOM_TEMPLATES_DIRECTORY="/var/lib/marzban/templates/"
   SUBSCRIPTION_PAGE_TEMPLATE="subscription/index.html"
   ```

۳. **ریستارت کردن مرزبان**
   ```sh
   marzban restart
   ```