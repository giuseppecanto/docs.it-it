---
title: "&lt;mexHttpsBinding&gt; | Microsoft Docs"
ms.custom: ""
ms.date: "03/30/2017"
ms.prod: ".net-framework-4.6"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "dotnet-clr"
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: f2ed3774-78b9-4a15-b79b-655f1ad68b86
caps.latest.revision: 8
author: "Erikre"
ms.author: "erikre"
manager: "erikre"
caps.handback.revision: 8
---
# &lt;mexHttpsBinding&gt;
Specifica le impostazioni per un'associazione usata per lo scambio di messaggi WS\-MetadataExchange \(WS\-MEX\) tramite HTTPS.  
  
## Sintassi  
  
```  
  
<mexHttpsBinding>  
   <binding   
       closeTimeout="TimeSpan"   
       name="string"   
       openTimeout="TimeSpan"   
       receiveTimeout="TimeSpan"  
       sendTimeout="TimeSpan">  
   </binding>  
</mexHttpsBinding>  
```  
  
## Attributi ed elementi  
 Nelle sezioni seguenti vengono descritti gli attributi, gli elementi figlio e gli elementi padre.  
  
### Attributi  
  
|Attributo|Descrizione|  
|---------------|-----------------|  
|`closeTimeout`|Valore <xref:System.TimeSpan> che specifica l'intervallo di tempo fornito per il completamento di un'operazione di chiusura.  Questo valore deve essere maggiore o uguale a <xref:System.TimeSpan.Zero>.  L'impostazione predefinita è 00:01:00.|  
|`name`|Stringa che contiene il nome della configurazione dell'associazione.  Questo valore deve essere univoco perché viene usato per identificare l'associazione.  Ciascuna associazione è provvista di un attributo `name` e `namespace` che insieme la identificano in modo univoco nei metadati del servizio.  In aggiunta, il nome è univoco fra associazioni dello stesso tipo.  A partire da [!INCLUDE[netfx40_short](../../../../../includes/netfx40-short-md.md)], non è necessario che le associazioni e i comportamenti dispongano di un nome.  Per altre informazioni sulla configurazione predefinita e le associazioni e i comportamenti senza nome, vedere [Configurazione semplificata](../../../../../docs/framework/wcf/simplified-configuration.md) e [Configurazione semplificata per servizi WCF](../../../../../docs/framework/wcf/samples/simplified-configuration-for-wcf-services.md).|  
|`openTimeout`|Valore <xref:System.TimeSpan> che specifica l'intervallo di tempo fornito per il completamento di un'operazione di apertura.  Questo valore deve essere maggiore o uguale a <xref:System.TimeSpan.Zero>.  L'impostazione predefinita è 00:01:00.|  
|`receiveTimeout`|Valore <xref:System.TimeSpan> che specifica l'intervallo di tempo fornito per il completamento di un'operazione di ricezione.  Questo valore deve essere maggiore o uguale a <xref:System.TimeSpan.Zero>.  L'impostazione predefinita è 00:10:00.|  
|`sendTimeout`|Valore <xref:System.TimeSpan> che specifica l'intervallo di tempo fornito per il completamento di un'operazione di invio.  Questo valore deve essere maggiore o uguale a <xref:System.TimeSpan.Zero>.  L'impostazione predefinita è 00:01:00.|  
  
### Elementi figlio  
 Nessuno.  
  
### Elementi padre  
  
|Elemento|Descrizione|  
|--------------|-----------------|  
|[\<associazioni\>](../../../../../docs/framework/configure-apps/file-schema/wcf/bindings.md)|Questo elemento contiene una raccolta di associazioni standard e personalizzate.|  
  
## Note  
 Questa associazione fondamentalmente un'associazione `WSHttpBinding` che supporta la sicurezza a livello di trasporto mediante certificati.  Per altre informazioni sulla configurazione e sull'utilizzo di un tale endpoint di metadati, vedere [Procedura: configurare un'associazione WS\-Metadata Exchange personalizzata](../../../../../docs/framework/wcf/extending/how-to-configure-a-custom-ws-metadata-exchange-binding.md), [Procedura: recuperare metadati attraverso un'associazione non MEX](../../../../../docs/framework/wcf/extending/how-to-retrieve-metadata-over-a-non-mex-binding.md) e l'esempio [Endpoint di metadati protetto personalizzato](../../../../../docs/framework/wcf/samples/custom-secure-metadata-endpoint.md).  
  
## Vedere anche  
 <xref:System.ServiceModel.Description.MetadataExchangeBindings.CreateMexHttpsBinding%2A>   
 <xref:System.ServiceModel.Configuration.MexHttpsBindingElement>   
 [Procedura: pubblicare metadati per un servizio usando un file di configurazione](../../../../../docs/framework/wcf/feature-details/how-to-publish-metadata-for-a-service-using-a-configuration-file.md)   
 [Pubblicazione e recupero di metadati su un'associazione personalizzata](../../../../../docs/framework/wcf/extending/publishing-and-retrieving-metadata-over-a-custom-binding.md)   
 [Procedura: configurare un'associazione WS\-Metadata Exchange personalizzata](../../../../../docs/framework/wcf/extending/how-to-configure-a-custom-ws-metadata-exchange-binding.md)   
 [Procedura: recuperare metadati attraverso un'associazione non MEX](../../../../../docs/framework/wcf/extending/how-to-retrieve-metadata-over-a-non-mex-binding.md)   
 [Endpoint di metadati protetto personalizzato](../../../../../docs/framework/wcf/samples/custom-secure-metadata-endpoint.md)   
 [Metadata](../../../../../docs/framework/wcf/feature-details/metadata.md)   
 [Associazioni](../../../../../docs/framework/wcf/bindings.md)   
 [Configurazione di associazioni fornite dal sistema](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)   
 [Using Bindings to Configure Windows Communication Foundation Services and Clients](http://msdn.microsoft.com/it-it/bd8b277b-932f-472f-a42a-b02bb5257dfb)   
 [\<associazione\>](../../../../../docs/framework/misc/binding.md)