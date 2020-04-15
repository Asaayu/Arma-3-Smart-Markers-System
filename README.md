# Arma 3 Smart Markers System
A smart marker system based on the Arma 3 Apex Old Man smart marker system.
## Adding smart markers to your content 
#### Adding to your mod
To add smart markers to your mod you will need to do the following,
- Create a `smart_markers` class in the base config file
- Add your markers as children classes following the format below
#### Adding to your mission
To add smart markers to your mission you will need to do the following,
- Create a `smart_markers` class in your description.ext file
- Add your markers as children classes following the format below

## Marker Class Format
```
class NAME
{
        position[] = POS;
        type = ICON;
        color_background = COLOR_BACKGROUND;
        color_icon = COLOR_ICON;
        max_zoom = ZOOM;
        displayname = TOOLTIP_TITLE;
        image = TOOLTIP_IMAGE;
        description = TOOLTIP_DESCRIPTION;
};
```
#### You will need to edit the snippet with the following items

**NAME** - A unique name for your marker

**POS** - The position where the marker will be created, (Make sure you use {} brackets rather then [] as they will not work in the config files)

**ICON** - A classname in CfgMarkers which will be the icon shown on the marker

**COLOR_BACKGROUND** - A classname in CfgMarkerColors which will be the color of the background square

**COLOR_ICON** - A classname in CfgMarkerColors which will be the color of the icon

**ZOOM** - A number between 0-1 which is the maximum zoom that the marker will be visable, use to avoid excess clutter when zooming out on the map.

**TOOLTIP_TITLE** - Text which will be used as the title for the map tooltip, if it is a localization key then it will be localized using the stringtable

**TOOLTIP_IMAGE** - Text which will be used as the file path for the map tooltip image. Make sure your images are 2^n and in paa/jpg format

**TOOLTIP_DESCRIPTION** - Text which will be used as the description for the map tooltip, if it is a localization key then it will be localized using the stringtable
