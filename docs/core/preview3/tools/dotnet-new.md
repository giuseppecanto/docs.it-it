---
title: Comando dotnet-new | Microsoft Docs
description: Il comando dotnet-new consente di creare nuovi progetti .NET Core nella directory corrente.
keywords: dotnet-new, interfaccia della riga di comando, comando dell&quot;interfaccia della riga di comando, .NET Core
author: blackdwarf
ms.author: mairaw
ms.date: 10/12/2016
ms.topic: article
ms.prod: .net-core
ms.technology: dotnet-cli
ms.devlang: dotnet
ms.assetid: fcc3ed2e-9265-4d50-b59e-dc2e5c190b34
translationtype: Human Translation
ms.sourcegitcommit: 2ad428dcda9ef213a8487c35a48b33929259abba
ms.openlocfilehash: d4ca76f3de38b5d05868292d5c4bb8e3b0c7fdf2

---

#<a name="dotnet-new-tooling-preview-4"></a>dotnet-new (strumenti dell'anteprima 4)

> [!WARNING]
> Questo argomento si applica agli strumenti dell'anteprima 4 di .NET Core (Visual Studio 2017 RC). Per gli strumenti dell'anteprima 2 di .NET Core, vedere l'argomento [dotnet-new](../../tools/dotnet-new.md).

## <a name="name"></a>Nome
dotnet-new: consente di creare un nuovo progetto .NET Core nella directory corrente.

## <a name="synopsis"></a>Riepilogo
`dotnet new [--help] [--type] [--lang]`

## <a name="description"></a>Descrizione
Il comando `dotnet new` rappresenta un modo pratico per inizializzare un progetto .NET Core valido e include l'esempio di codice sorgente per provare il set di strumenti dell'interfaccia della riga di comando. 

Questo comando viene richiamato nel contesto di una directory. Quando richiamato, il comando avrà come risultato il rilascio dei due elementi principali nella directory corrente: 

1. Un file `Program.cs` (o `Program.fs`) contenente un programma "Hello World" di esempio.
2. Un file di progetto csproj valido.

Dopo questa operazione, il progetto è pronto per essere compilato e/o ulteriormente modificato. 

## <a name="options"></a>Opzioni

`-h|--help`

Stampa una breve guida per il comando.  

`-l|--lang C#`

Linguaggio del progetto. Il valore predefinito è `C#`. Altri valori validi sono `csharp` e `cs`.

`-t|--type`

Tipo di progetto. I valori validi per C# sono `console`, `web`, `lib` e `xunittest`, mentre per F# è valido solo `console`. 

## <a name="examples"></a>Esempi

Creare un progetto di applicazione console C# nella directory corrente:

`dotnet new` o `dotnet new --lang c#` 
   
Creare un nuovo progetto di applicazione console ASP.NET Core C# nella directory corrente:

`dotnet new -t web`


<!--HONumber=Jan17_HO3-->

