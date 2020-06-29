---
title: Entwickeln mit Q# und .Net
author: bradben
ms.author: bradben
ms.date: 5/30/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 2b0b16bdd9fccc3b668036e6df2b20e11b32f8b6
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274086"
---
# <a name="develop-with-q-and-net"></a>Entwickeln mit Q# und .Net

Q# ist auf die Verwendung mit .NET-Sprachen wie C# und F# ausgelegt.
In diesem Leitfaden wird veranschaulicht, wie Sie Q# mit einem in einer .NET-Sprache geschriebenen Hostprogramm verwenden.

## <a name="prerequisites"></a>Voraussetzungen

- Installieren Sie das Quantum Development Kit [für die Nutzung mit Q#-Befehlszeilenprojekten](xref:microsoft.quantum.install.standalone).

## <a name="creating-a-q-library-and-a-net-host"></a>Erstellen einer Q#-Bibliothek und eines .NET-Hosts

Der erste Schritt ist die Erstellung von Projekten für Ihre Q#-Bibliothek und für den .NET-Host, von dem Aufrufe für die in Ihrer Q#-Bibliothek definierten Vorgänge und Funktionen durchgeführt werden.

### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

- Erstellen einer neuen Q#-Bibliothek
  - Klicken Sie auf **Datei** -> **Neu** -> **Projekt**.
  - Geben Sie im Suchfeld als Suchbegriff „Q#“ ein.
  - Wählen Sie **Q#-Bibliothek** aus.
  - Wählen Sie **Weiter** aus.
  - Wählen Sie einen Namen und Speicherort für Ihre Bibliothek aus.
  - Stellen Sie sicher, dass die Option „Place project and solution in same directory“ (Projekt und Projektmappe in demselben Verzeichnis anordnen) **deaktiviert** ist.
  - Klicken Sie auf **Erstellen**
- Erstellen eines neuen C#- oder F#-Hostprogramms
  - Navigieren Sie zu **Datei** > **Neu** > **Projekt**.
  - Wählen Sie für C# bzw. F# die Option „Konsolen-App (.NET Core)“ aus.
  - Wählen Sie **Weiter** aus.
  - Wählen Sie unter *Projektmappe* die Option „Zur Projektmappe hinzufügen“ aus.
  - Wählen Sie einen Namen für Ihr Hostprogramm aus.
  - Klicken Sie auf **Erstellen**

### <a name="visual-studio-code-or-command-line"></a>[Visual Studio Code oder Befehlszeile](#tab/tabid-cmdline)

- Erstellen einer neuen Q#-Bibliothek

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- Erstellen Sie ein neues C#- oder F#-Konsolenprojekt.

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- Fügen Sie Ihre Q#-Bibliothek als Verweis aus Ihrem Hostprogramm hinzu.

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- [Optional] Erstellen Sie eine Projektmappe für beide Projekte.

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

***

## <a name="calling-into-q-from-net"></a>Durchführen von Q#-Aufrufen aus .NET

Nachdem Sie Ihre Projekte gemäß der obigen Anleitung eingerichtet haben, können Sie aus Ihrer .NET-Konsolenanwendung Q#-Aufrufe durchführen.
Der Q#-Compiler erstellt .NET-Klassen für alle Q#-Vorgänge und -Funktionen, die Ihnen das Ausführen Ihrer Quantenprogramme in einem Simulator ermöglichen.

Das [Beispiel zur .NET-Interoperabilität](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) enthält das folgende Beispiel für einen Q#-Vorgang:

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

Um diesen Vorgang aus .NET in einem Quantensimulator aufzurufen, können Sie die Methode `Run` der .NET-Klasse `RunAlgorithm` verwenden, die vom Q#-Compiler generiert wird:

### <a name="c"></a>[C#](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[F#](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie das Quantum Development Kit nun sowohl für Q#-Befehlszeilenprogramme als auch für die Interoperabilität mit .NET eingerichtet haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.
