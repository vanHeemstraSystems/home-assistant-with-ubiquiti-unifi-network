# 100 - Install the UniFi Integration in Home Assistant

## 100 - Automatically

Visit https://home-assistant.io/integrations/unifi and click the button **ADD INTEGRATION TO MY HOME ASSISTANT**.

When asked to enter your Home Assistant URL, enter ```http://10.211.55.4:8123``` (in our case, check yours) and choose **Save**.

When prompted: ```Open page in your Home Assistant?```, click **Open link**.

Inside Home Assistant (https://10.211.55.4:8123/config/integrations/dashboard) you will se a dialogue window that states: ```Do you want to set up UniFi Network?``. Click **OK**.

## 200 - Manually
 
Inside Home Assistant go to **Settings** > **Devices & Services**.

Under the tab ```Integrations```, if the **Ubiquiti** Integration is not yet listed, click **+ ADD INTEGRATION**.

In the Search field enter: **Ubiquiti**. The Integration with the same name should show, click the entry.

You will be presented with a list of Ubiquiti integrations:

- UniFi Network
- UniFi Protect
- UniFi AP (Access Point)
- UniFi LED

In our case, click ```UniFi Network```.

## 300 - In both cases, continue as follows

**NOTE**: You will need to have set up a **local user with password** on one of your UniFi Cloud Gateways (here: UniFi Express), before you can log in from Home Assistant! You can add a local user via [OS Settings > Admins](https://unifi.ui.com/consoles/942A6F0EB0C20000000007E83892000000000852CCED0000000065A3FE78:1406079628/admins/users)

![local-admin](https://github.com/vanHeemstraSystems/home-assistant-with-ubiquiti-unifi-network/assets/1499433/d2134508-885d-41e1-a026-82e3602ffe8f)

You will presented with a form.

Host: **192.168.1.1** (The I.P. Address of our UniFi Express, or use **unify** as a hostname instead)

Username: **local-admin**

Password: ******* (the password you created for the ```local-admin``` user in UniFi OS)

Port: **443**

Leave the checkbox empty for ```Verify SSL certificate```.

Click **SUBMIT**

If shown a prompt **UniFi Network**, click **SUBMIT** on the dialogue window.

After a few seconds, you hopefully see a dialogue window: **Success!**

It will list the devices, here:

- UniFi WLAN (Ubituiti Networks)
- UniFi Express UX (Ubiquiti Networks)
- UniFi Network Application (Ubiquiti Networks)

You can choose Areas to assign these devices to or simply click **FINISH**.

A new integration card will now show at your Integrations, named **UniFi Network**.

Click on it for further configuration.

## 400 - Configure UniFi Network Integration

When clicking on **Configuration** on the UniFi Network Integration, I was prompted if I wanted to create entities from the wired linked TP-Link Router. Your network set up may differ, so use this only as a use case.

I agreed to creating Entities from the TP-Link Router.

Next, I ticked the following check boxes on the **UniFi Network options 1/3** dialogue window:

Configure device tracking:

[ X ] Track network clients

[ X ] Include wired network clients

[ X ] Track network devices (Ubiquiti devices)

Select SSIDs to track wireless clients on 

[ X ] UniFi (the name I gave to my UniFi local WiFi network, yours may differ)

Time in seconds from last seen until considered away: 300

[ ] Disable UniFi Network wired bug logic

Click **NEXT**

Next, I ticked the following check boxes on the **UniFi Network options 2/3** dialogue window:

Configure client controls

Create switches for serial numbersyou want to control network access for.

Network access controlled clients

[ X ] TP-Link Router (30:de:4b:a2:14:77) - Note: I have this router, you may not.

[ X ] Allow control of DPI restriction groups

Click **NEXT**

Lastly, I ticked the following check boxes on the **UniFi Network options 3/3** dialogue window:

Configure statistics sensors.

[ X ] Bandwidth usage sensors for network clients

[ X ] Uptime sensors for network clients

Click **SUBMIT**

You will be prompted: **Success!**

Options successfully saved.

Click **FINISH**

You are done!

You can now click through your devices

## 500 - Further reading

Recommended reading **Home Assistant automations based on WiFi connection status** at https://www.youtube.com/watch?v=K4CEsp6tBcE
