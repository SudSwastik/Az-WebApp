### Steps To Deploy A .Net Core Application To Azure Web App

>Create a resource Group
```
$ az group create -l centralus -n <name-of-resource-group>
```

>Create a App Plan
```
$ az appservice plan create -l centralus -g <name-of-resource-group> -n <name-of-webapp-plan> --sku <Free-Plan>(F1)
```

>Create a Web App In the App Plan
```
$ az webapp create -g <name-of-resource-group> --plan <name-of-webapp-plan> -n <name-of-webapp>
```

>Deployment Of Project To Web App
```
$ az webapp deployment source config -n <name-of-webapp> --repo-url <Git Url Of Project> --branch master
```
