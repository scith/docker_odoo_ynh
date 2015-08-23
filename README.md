Dockerized Odoo for YunoHost
----------------------------
Warning: This YunoHost app is still in development. Use it at your own risk! I am **not** responsible for any data loss that jeopardizes your organization


**WARNING**: Odoo is a complex app. **DO NOT USE IT** to run your business unless you know what you are doing!!! If you don't, use <a href="https://www.odoo.com/fr_FR/pricing-online#num_users=1&custom_apps=0">the hosted Odoo</a> that will give you peace and customer support!


**Important:** This app MUST be installed on a domain's root!
https://odoo.example.com/ will work
https://example.com/odoo/ will NOT work

What does not work
------------------
Backup and restore
Login via YunoHost (you have to create user accounts in Odoo)
Autostart at server restart *might* not work

Odoo
----

Odoo is a suite of web based open source business apps.

The main Odoo Apps include an <a href="https://www.odoo.com/page/crm">Open Source CRM</a>, <a href="https://www.odoo.com/page/website-builder">Website Builder</a>, <a href="https://www.odoo.com/page/e-commerce">eCommerce</a>, <a href="https://www.odoo.com/page/project-management">Project Management</a>, <a href="https://www.odoo.com/page/accounting">Billing &amp; Accounting</a>, <a href="https://www.odoo.com/page/point-of-sale">Point of Sale</a>, <a href="https://www.odoo.com/page/employees">Human Resources</a>, Marketing, Manufacturing, Purchase Management, ...  

Odoo Apps can be used as stand-alone applications, but they also integrate seamlessly so you get
a full-featured <a href="https://www.odoo.com">Open Source ERP</a> when you install several Apps.

Install procedure
----
First, you should add the subdomain to you yunohost configuration. For instance, we use odoo.domain.org.
 _Domain creation failed at some point when it has been done from the web adminstration inteface._
```sudo yunohost domain add odoo.domain.org```
Then you can run
```sudo yunohost install https://github.com/scith/docker_odoo_ynh.git```
You will be asked for the domain
```Choisissez un domaine pour Odoo (Odoo sera installé dans sa racine !) : odoo.domain.org```
You will be asked if it's a public instance (Direct acces without yunohost authentification). Be carefull because your website will be exposed and you should modify the default passwords.

 Then, it should work, you just need to got to
 odoo.domain.org to access to the database management page.
