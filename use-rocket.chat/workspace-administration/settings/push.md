# Push

Enable and configure push notifications for your workspace members using mobile devices.

{% hint style="info" %}
By default, community workspaces come with 10,000 free monthly push notifications. If you need more, please [contact us](https://www.rocket.chat/sales-contact) to discuss upgrading to an Enterprise plan.
{% endhint %}

## Push Notifications Configuration

{% hint style="info" %}
To be able to use push notifications, you are required to accept the **Cloud Service Privacy Terms Agreement** in the **Administration** > **Workspace** > **Settings** > **Setup Wizard** > **Cloud Info** settings.
{% endhint %}

To enable push notifications, go to **Administration > Workspace > Settings > Push.**

* **Enable**: Turn on to enable push notifications on your Rocket.Chat instance
* **Enable Gateway**: Setting this to true allows you to use a custom push notification gateway

{% hint style="info" %}
Rocket.Chat SaaS workspaces use the Rocket.Chat gateway by default and cannot be changed.

On self-managed workspaces, you can either use the default Rocket.Chat gateway or set up a custom notification gateway.
{% endhint %}

* **Gateway**: Specify the gateway to use. Multiple lines can be used to specify multiple gateways
* **Production:** Enable this for workspaces in production

With the configuration all done, you can **Send a test push to my user** to send a test push to yourself.

{% hint style="info" %}
To successfully send a test push to your user, you need to be logged in to the workspace on your mobile device and then close or minimize the application.
{% endhint %}

### Certificate and Keys

* **APN Passphrase**: The passphrase required for authenticating with Apple's push notification servers.
* **APN Key**:  The Apple Push Notification Service key.
* **APN Cert**: The Apple Push Notification Service certificate  required to send push notifications to iOS devices.
* **APN Dev Passphrase**: The password used to protect your APNs development certificate.
* **APN Dev Key**: The Apple Push Notification Service development key.
* **APN Dev Cert:** The certificate used for development purposes to authenticate an app with Apple's push notification service to send push notifications to iOS devices.
* **GCM API Key**: The key used to authenticate an app with Google's Cloud Messaging service to send push notifications to Android devices.
* **GCM Project Number:** The unique identifier for your Google Cloud Platform project used to authenticate your app with Google's Cloud Messaging service.

### Privacy

In Privacy, you can configure what information you want your push notification to have.

* **Show Channel/Group/Username in Notification**: Toggle this on to make the channel name, group name, and username visible in notifications.
* **Show Message in Notification**: Enabling this makes messages visible in notifications.
* **Hide message content from Apple and Google (and the Gateway, if enabled)**: Turn this on to hide the content of a message from Google/Apple or any other push gateway.\
  This adds only the message id to the notification data. The mobile client dynamically fetches the content from the server and updates the notification before displaying it.

{% hint style="info" %}
For [Enterprise workspaces](enterprise.md), failure in fetching a message using the `message id` provided in the push data results in a "You have a new message" being sent.
{% endhint %}

With the push configuration completed, follow the  [#default-user-preferences](account-settings/#default-user-preferences "mention") guide to set the default user preferences for notinotificationsfication. Manage channel-based notifications using the [#channel-notifications](../../user-guides/rooms/channels/edit-a-channel.md#channel-notifications "mention") guide.

{% hint style="info" %}
On some channels, notifications can stop if the number of users exceeds the set limit. You can set the limit in **Administration** > **General** > **Notifications**. See[#notifications](general/#notifications "mention") for more information.
{% endhint %}

## Connect to cloud

When you purchase a  package for push notifications as a self-managed customer, you need to connect your workspace [Rocket.Chat Cloud](../../rocket.chat-cloud/).

Link and sync your account in the Connectivity Services menu.

{% content-ref url="../registration.md" %}
[registration.md](../registration.md)
{% endcontent-ref %}

## Check the count of notifications used per month

To check the count of notifications used per month:

* Go to [cloud.rocket.chat](http://cloud.rocket.chat)
* Switch to the Workspaces tab
* Select the workspace you want to check the count for
* The push notifications block shows the number of used notifications per your current limit per month.
