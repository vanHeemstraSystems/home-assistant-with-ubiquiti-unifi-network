# 100 - Install the UniFi Integration in Home Assistant

## 100 - Automatically

Visit https://home-assistant.io/integrations/unifi and click the button **ADD INTEGRATION TO MY HOME ASSISTANT**.

When asked to enter your Home Assistant URL, enter ```10.211.55.4``` (in our case, check yours) and choose **Save**.

...

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

You will presented with a form.

Host: **192.168.1.1** (The I.P Address of our UniFi Express)

Username: **wvanheemstra@icloud.com**

Password: ******* (the password you signed up with with UniFi Network)

Port: **443**

Leave the checkbox empty for ```Verify SSL certificate```.

Click **SUBMIT**

If shown a prompt **UniFi Network**, click **SUBMIT** on the dialogue window.
