# dpe
"Distributed" Promotions Engine (POC)

 - Drupal 8
 - Commerce 2
 - REST API

**Environment by `Drudock`**

https://github.com/4AllDigital/DruDockCli

```
curl -O http://d1gem705zq3obi.cloudfront.net/drudock.phar && \
mv drudock.phar /usr/local/bin/drudock && \
chmod +x /usr/local/bin/drudock && \
drudock
```

Install  and setup instructions (All `drudock` commands must be run from project root).

 - `drudock app:init:containers`
    - wait for container download and start
 - `drudock nginx:proxy:start`
    - wait for container restart and proxy network to be running 
 - `drudock mysql:import`
    - select mysql .sql import and wait for mysql import to complete
 - `cd app && composer install`
    - wait for dependencies to be downloaded to vendor directory.
 - `drudock app:bash php`
    - this will start bash session in php container
 - `drush status`
    - should return default drupal installation status
 - `drush uli`
    - generate's uli open `http://dpe.localhost/<ULI>` in your favourite browser.
    
REST API
 - Installation comes with 2 example promotions, each with example coupons.
 - Open http://dpe.localhost/api/1.0/promotions?_format=json in a browser to see initial JSON API response for active promotions.
    
    
**setup and committed in 65 mins 09 seconds.**
    