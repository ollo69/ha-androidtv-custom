# HA Android TV Custom integration
This custom integration is the copy of the [Android TV](https://www.home-assistant.io/integrations/androidtv) integration
implemented in Home Assistant with the additional option to define **custom commands** as supported by the 
library [python-androidtv](https://github.com/JeffLIrion/python-androidtv) used both by this and native integration.</br>

The aim is to allow tests and find the final solution to provide support to currently unsupported AndroidTV device, 
to finally move back to the HA native integration.

Obviously, feedback is important, we can use [issue section](https://github.com/ollo69/ha-androidtv-custom/issues) in this 
repository or open a discussion on the [community forums](https://community.home-assistant.io/) or Discord chat. 

## Installation & configuration
You can install this integration in two ways: via HACS or manually.

### Option A: Installing via HACS
If you have HACS, you must add this repository ("https://github.com/ollo69/ha-androidtv-custom") to your Custom Repository 
selecting the Configuration Tab in the HACS page.
After this you can go in the Integration Tab and search the "Android TV Custom" component to configure it.

### Option B: Manually installation (custom_component)
1. Clone the git master branch.
1. Unzip/copy the androidtv_custom directory within the `custom_components` directory of your homeassistant installation.
The `custom_components` directory resides within your homeassistant configuration directory.
Usually, the configuration directory is within your home (`~/.homeassistant/`).
In other words, the configuration directory of homeassistant is where the configuration.yaml file is located.
After a correct installation, your configuration directory should look like the following.
    ```
    └── ...
    └── configuration.yaml
    └── secrects.yaml
    └── custom_components
        └── androidtv_custom
            └── __init__.py
            └── media_player.py
            └── ...
    ```

    **Note**: if the custom_components directory does not exist, you need to create it.
    
## Component setup    

For the configuration use exactly the same options used to configure the standard AndroidTV component, however choosing 
the Android TV Custom component from the list of integrations.

**N.B. Before configuring this integration, remove the standard Android TV integration.**
