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

You will presented with a form.

Host: **192.168.1.1** (The I.P. Address of our UniFi Express)

Username: **wvanheemstra@icloud.com**

Password: ******* (the password you signed up with with UniFi Network)

Port: **443**

Leave the checkbox empty for ```Verify SSL certificate```.

Click **SUBMIT**

If shown a prompt **UniFi Network**, click **SUBMIT** on the dialogue window.
