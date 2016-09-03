# OpenHAB

This is my home automation setup. I'm using OpenHAB(1) together with habmin.

## Docker
I'm an extensive docker user, if you want to try this without installing to much stuff, just use my docker-compose.yml file with `docker-compose up -d` in this dir. Then `docker-compose logs` to see the output from your container.

## Config files:
The basic configs are sitemap/home.sitemap and home.items. However, I wanted sunrise/sunset to toggle lights on and off, so thats why weather.items is also included. This is also an homekit.sitemap, which is needed for the homekit mapping (i.e. Siri).

## Habmin
Config files are as confusing as the habmin interface, but that was the easiest way to actually add and rename the z-wave items (Configuration, Items and Groups, Bindings). The names in the item list is what you use in your sitemap.

## Homekit / Siri
Install [OpenHAB-HomeKit-Bridge](https://github.com/htreu/OpenHAB-HomeKit-Bridge), and tweak the homekit.sitemap to map into the items you want to control with Siri. Since you will tell Siri the names, they need to be different from each other, otherwise you will struggle with your lamps a lot...

### App
I use Insteon+ for mapping what Siri sees with the names, so that I don't have to change the config file. This is supposedly being fixed in iOS 10.

## Z-wave
Controller: 
* Z-Wave Me UZB Z-Wave Plus USB Stick Controller (EU-version), lowest price on eBay.

Nodes:
* Smart Plug - NodOn (NO-ASP-3-1-10). *Please note that these do not have power meters.*
* Remote Control - Duwi (DUW_064459). *Just wanted to have something physical with buttons to test with.*


