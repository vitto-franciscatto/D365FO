# Database snapshot to keep cenario for debbuging purposes

##	Limpar todas as alterações do controle de versão.

##	Listar todos os arquivos .AxModels enviados.

##	Fazer backup das models que estiverem presentes no ZIP.

##	Aplicar a nova versão da máquina via LCS.

##	Aplicar o DeployPackage por dentro da VM.

- O processo apresentará erro e não importará as models. Porém, ele importa as ISVs, sendo importante para manter a base atualizada.

##	Parar os serviços do ambiente:

-	Parar os serviços pelo Services.

-	Executar no CMD: iisreset /stop

##	Remover da PackagesLocalDirectory as models que serão atualizadas.

##	Importar as novas versões das models utilizando o script:

```
Import-AXModel -File "C:\Temp\FagronCore.axModel"
```

##	Rodar um Full Build e ajustar as referências, se necessário.

- Caso ocorra algum problema grande, o Mardonio possui fácil acesso ao pessoal do EMEA.

##	Comparar model a model as alterações realizadas pelo controle de versão.

- Nesse momento, também é importante avaliar as ISVs.

##	Disponibilizar o ambiente para testes.
