---
title: "Elemento &lt;add&gt; per schemeSettings (impostazioni URI) | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
  - "jsharp"
ms.assetid: 594a7b3b-af23-4cfa-b616-0b2dddb1a705
caps.latest.revision: 7
author: "mcleblanc"
ms.author: "markl"
manager: "markl"
caps.handback.revision: 7
---
# Elemento &lt;add&gt; per schemeSettings (impostazioni URI)
Aggiunge un'impostazione dello schema per un nome di schema.  
  
## Sintassi  
  
```  
  
      <add   
   name = "http|https" genericUriParserOptions="DontUnescapePathDotsAndSlashes"  
/>  
```  
  
## Attributi ed elementi  
 Nelle sezioni seguenti vengono descritti attributi, elementi figlio ed elementi padre.  
  
### Attributi  
  
|Attribute|Descrizione|  
|---------------|-----------------|  
|name|Il nome dello schema per il quale si applica questa impostazione.  Gli unici valori supportati sono name\="http" e name\="https".|  
  
## Attributo {nome attributo}  
  
|Valore|Descrizione|  
|------------|-----------------|  
|genericUriParserOptions|Le opzioni del parser per questo schema.  L'unico valore supportato è genericUriParserOptions\= "DontUnescapePathDotsAndSlashes".|  
  
### Elementi figlio  
 None  
  
### Elementi padre  
  
|Elemento|Descrizione|  
|--------------|-----------------|  
|[Elemento \<schemeSettings\> \(impostazioni URI\)](../../../../../docs/framework/configure-apps/file-schema/network/schemesettings-element-uri-settings.md)|Specifica come un oggetto <xref:System.Uri> verrà analizzato per schemi specifici.|  
  
## Note  
 Per impostazione predefinita, la classe <xref:System.Uri?displayProperty=fullName> priva dei caratteri escape i delimitatori del percorso con codifica percentuale prima di eseguire la compressione del percorso.  È stato implementato come meccanismo di sicurezza rispetto ad attacchi simili ai seguenti:  
  
 `http://www.contoso.com/..%2F..%2F/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 Se questo URI viene passato lungo i moduli che non gestiscono correttamente i caratteri codificati in percentuale, potrebbe verificarsi che il comando seguente venga eseguito dal server:  
  
 `c:\Windows\System32\cmd.exe /c dir c:\`  
  
 Per questo motivo, la classe <xref:System.Uri?displayProperty=fullName> come prima cosa priva dei caratteri escape i delimitatori del percorso, quindi applica compressione del percorso.  Il risultato di passare l'URL dannoso al costruttore di classe <xref:System.Uri?displayProperty=fullName> è il seguente URI:  
  
 `http://www.microsoft.com/Windows/System32/cmd.exe?/c+dir+c:\`  
  
 È possibile modificare questo comportamento predefinito per non consentire l'escape dei delimitatori del percorso con codifica percentuale utilizzando l'opzione di configurazione schemeSettings per uno specifico schema.  
  
## File di configurazione  
 L'elemento può essere utilizzato nel file di configurazione dell'applicazione o nel file di configurazione del computer \(Machine.config\).  
  
## Esempio  
 Nell'esempio di codice seguente viene mostrata una configurazione utilizzata dalla classe <xref:System.Uri> per il supporto di non eseguire l'operazione di escape dei delimitatori di percorso con codifica percentuale dello schema HTTP.  
  
```  
<configuration>  
  <uri>  
    <schemeSettings>  
      <add name="http" genericUriParserOptions="DontUnescapePathDotsAndSlashes"/>  
    </schemeSettings>  
  </uri>  
</configuration>  
```  
  
## Vedere anche  
 <xref:System.Configuration.SchemeSettingElement?displayProperty=fullName>   
 <xref:System.Configuration.SchemeSettingElementCollection?displayProperty=fullName>   
 <xref:System.Configuration.UriSection?displayProperty=fullName>   
 <xref:System.Configuration.UriSection.SchemeSettings%2A?displayProperty=fullName>   
 <xref:System.GenericUriParserOptions?displayProperty=fullName>   
 <xref:System.Uri?displayProperty=fullName>   
 [Schema delle impostazioni di rete](../../../../../docs/framework/configure-apps/file-schema/network/index.md)