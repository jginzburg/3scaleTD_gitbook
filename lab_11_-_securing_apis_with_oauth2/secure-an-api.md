## Secure an API using OpenID Connect

* Go back to **3scale admin console** (https://3scale-admin.3scale.{{ book.suffix }}.
* Login as admin/admin.
* Click on the **APIs** tab.
* Expand the **Products** API.
* Click on **Integration**.

![](../assets/Selection_451.png)

* Click on **edit integration settings**.

![](../assets/Selection_452.png)

* Scroll down to the bottom of the page.
* Click on **OpenID Connect**.
* Click on the **Update Service** button.
* Accept the warning.

![](../assets/Selection_453.png)

* Click on **edit APIcast configuration**.

![](../assets/Selection_454.png)

* Expand the **Authentication Settings** section.
* Enter the following value for the **OpenID Conect Issuer**: http://3scale-client:&lt;Paste your CLIENT SECRET&gt;@sso-unsecured.{{ book.suffix }}/auth/realms/3scaleRealm

![](../assets/Selection_462.png)

* Scroll down to the bottom of the page.
* Click on the **Update the Staging Environment** button.
* Click on the **Back to Integration & Configuration** link.
* Click on the **Promote v.X to Production**.
* Click on the **Developers** tab.
* Click on the **RHBank2** account.

![](../assets/Selection_456.png)

* Click on the **4 Applications** breadcrumb link.
* Click on **Create Application**.

![](../assets/Selection_457.png)

* Enter the following values:

| Parameter | Value |
| --- | --- |
| **Application Plan** | ProductsPremiumPlan |
| **Name** | OIDCApp |
| **Description** | OIDC Secured Application |

* Click on the **Create Application** button.

![](../assets/Selection_458.png)

* Take note of the generated **Client ID**.
* Click on the **Change** link next to **Redirect URL** in the **API Credentials** section.
* Enter https://www.getpostman.com/oauth2/callback as the **Redirect URL** and click on the **Update** button.


![](../assets/Selection_463.png)


* Go back to the **Red Hat Single Sign-On** console ( https://sso.{{ book.suffix }}/auth/admin).
* Click on **Clients**.

{% hint style='tip' %}
There should be a new Client with the same ID as the created 3scale's Application Client ID. 

3scale can synchronize client credentials between 3scale (Application credentials) and a Red Hat Single Sign-On server using OpenID Connect (OIDC). 3scale utilizes a service called **Zync** to synchronize calls to the Red Hat Single Sign-On server.
{% endhint %}



