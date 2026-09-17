=========================Criar o web app==================
Subscription:
sua assinatura

Resource Group:
rg-deploy

Name:
fiap-cloud-static-XXXX

Publish:
Code

Runtime:
.NET 10 (LTS)

Operating System:
Windows

Region:
mesma região dos demais recursos


===============Compacte o conteudo da pasta==============
static-app.zip
└── index.html

===============Deploy====================================
Deployment Center
        ↓
Manual Deployment
        ↓
Publish files
        ↓
Selecionar static-app.zip
        ↓
Skip Server-Side Build = ON
        ↓
Save / Deploy
        ↓
Acessar pelo Default domain

