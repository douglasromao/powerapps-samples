# Fórmula para marcar um usuário como padrão em determinado campo do formulário
Geralmente utilizado para preencher o usuário atual em um campo de formulário

Na propriedade **Default** do DataCard, coloque o seguinte código:

```json
{
      '@odata.type': "#Microsoft.Azure.Connectors.SharePoint.SPListExpandedUser",
      Claims: Concatenate(
          "i:0#.f|membership|",
          User().Email
      ),
      DisplayName: User().FullName,
      Email: User().Email
}
```
 
