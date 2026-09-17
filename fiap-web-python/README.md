============================================
Cloud Solutions

Aplicação publicada no Azure App Service

Tecnologia: Python + Flask
Ambiente: Azure App Service
Versão: 1.0


==========================================
Subscription: sua assinatura

Resource Group:
rg-cloud-solutions

Name:
fiap-cloud-python-XXXX

Publish:
Code

Runtime stack:
Python 3.14

Operating System:
Linux

Region:
Sua região com permissão


==================================================
Quando você faz um ZIP Deploy, por padrão o App Service pode interpretar o ZIP como um pacote já pronto para execução e não executar automaticamente o processo de build.

Azure Portal
   ↓
App Service Python
   ↓
Settings
   ↓
Environment variables
   ↓
App settings
   ↓
+ Add

Name                            Value
------------------------------------------------
SCM_DO_BUILD_DURING_DEPLOYMENT  true

Linha de comando:
az webapp config appsettings set \
  --resource-group rg-cloud-solutions \
  --name fiap-cloud-python-XXXX \
  --settings SCM_DO_BUILD_DURING_DEPLOYMENT=true


==================================================

Azure Portal
   ↓
App Services
   ↓
fiap-cloud-python-XXXX
   ↓
Deployment
   ↓
Deployment Center   

Aguarde o deployment finalizar e acesse o endereço ou acesse via browse
fiap-cloud-python-f1754-dfcffqbtg9bngees.chilecentral-01.azurewebsites.net

  az webapp deploy \
  --resource-group rg-cloud-solutions \
  --name fiap-cloud-python-XXXX \
  --src-path python-app.zip \
  --type zip


Deployment via CLI/ZIP
→ SCM_DO_BUILD_DURING_DEPLOYMENT=true

Deployment via portal novo
→ Skip Server-Side Build = OFF




