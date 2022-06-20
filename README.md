<p align="center">
<a href="https://console.platform.sh/projects/create-project/?template=https://github.com/platformista/prestashop-psh/blob/master/template-definition.yaml&utm_campaign=deploy_on_platform?utm_medium=button&utm_source=affiliate_links&utm_content=https://github.com/platformista/prestashop-psh/blob/master/template-definition.yaml" target="_blank" title="Deploy with Platform.sh"><img src="https://platform.sh/images/deploy/deploy-button-lg-blue.svg"></a>
</p>


# Prestashop template for Flexible Web Publisher on Platform.sh

## How to install

1. Clone this repository
2. Create a new platform.sh project

```
platform project:create
```

3. Add specific environment variables

```
platform variable:create -y -p <project> -e master --level environment --name env:ADMIN_EMAIL --value your@email.com
platform variable:create -y -p <project> -e master --sensitive true --level environment --name env:ADMIN_PASSWORD --value yourpassword
```

4. Push to platform.sh

```
platform project:set-remote <project>
git push platform master
```

5. Backend

You can access your backend at `/admin-fwp` with the credentials that you defined as variables.
