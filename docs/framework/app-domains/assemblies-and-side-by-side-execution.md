---
title: Assembly ed esecuzione side-by-side | Microsoft Docs
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology:
- dotnet-bcl
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- side-by-side execution [.NET Framework]
- assemblies [.NET Framework], side-by-side execution
ms.assetid: e42036ee-7590-47d1-b884-cc856e39bd5d
caps.latest.revision: 10
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.translationtype: Machine Translation
ms.sourcegitcommit: 9f5b8ebb69c9206ff90b05e748c64d29d82f7a16
ms.openlocfilehash: 3b78c82937c78286302adef532c451c24987da39
ms.contentlocale: it-it
ms.lasthandoff: 06/02/2017

---
# <a name="assemblies-and-side-by-side-execution"></a>assembly ed esecuzione contemporanea di più versioni
L'esecuzione contemporanea di diverse versioni è la capacità di archiviare ed eseguire più versioni di un'applicazione o di un componente sullo stesso computer. Tale caratteristica consente di avere sullo stesso computer più versioni del runtime e più versioni delle applicazioni e dei componenti che utilizzano una versione del runtime. L'esecuzione contemporanea di diverse versioni offre un maggior controllo per definire a quale versione di un componente un'applicazione è associata, e quale sia la versione del runtime da essa utilizzata.  
  
 Il supporto per l'archiviazione e l'esecuzione contemporanea di diverse versioni dello stesso assembly è parte integrante della denominazione con nome sicuro ed è incorporato nell'infrastruttura del runtime. Poiché il numero di versione dell'assembly con nome sicuro è parte della relativa identità, il runtime può archiviare più versioni dello stesso assembly nella Global Assembly Cache e caricare tali assembly in fase di esecuzione.  
  
 Benché il runtime offra la possibilità di creare applicazioni predisposte all'esecuzione contemporanea di diverse versioni, questa non viene implementata automaticamente. Per altre informazioni sulla creazione di applicazioni per l'esecuzione side-by-side vedere [Linee guida per la creazione di componenti per l'esecuzione side-by-side](../../../docs/framework/deployment/guidelines-for-creating-components-for-side-by-side-execution.md).  
  
## <a name="see-also"></a>Vedere anche  
 [Come il runtime individua gli assembly](../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)   
 [Assembly in Common Language Runtime](../../../docs/framework/app-domains/assemblies-in-the-common-language-runtime.md)
