---
title: Entwickeln mit Q# und .NET
description: Hier erfahren Sie, wie Sie mithilfe von .NET-Sprachen eine Anwendung vom Typ Q# erstellen.
author: bradben
ms.author: v-benbra
ms.date: 8/20/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
no-loc:
- Q#
- $$v
ms.openlocfilehash: e8733918daa02afaea0fc1994d5f0851d4be9b93
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834328"
---
# <a name="develop-with-no-locq-and-net"></a>Entwickeln mit Q# und .NET

Q# ist auf die Verwendung mit .NET-Sprachen wie C# und F# ausgelegt.
In diesem Leitfaden wird veranschaulicht, wie Sie Q# mit einem in einer .NET-Sprache geschriebenen Hostprogramm verwenden.

Zunächst erstellen wir die Q#-Anwendung und den .NET-Host und veranschaulichen dann, wie Q# über den Host aufgerufen wird.

## <a name="prerequisites"></a>Voraussetzungen

- Installieren Sie das Quantum Development Kit [für die Nutzung mit Q#-Projekten](xref:microsoft.quantum.install.standalone).

## <a name="creating-a-no-locq-library-and-a-net-host"></a>Erstellen einer Q#-Bibliothek und eines .NET-Hosts

Der erste Schritt ist die Erstellung von Projekten für Ihre Q#-Bibliothek und für den .NET-Host, von dem Aufrufe für die in Ihrer Q#-Bibliothek definierten Vorgänge und Funktionen durchgeführt werden.

Folgen Sie den Anweisungen auf der Registerkarte, die Ihrer Entwicklungsumgebung entspricht.
Wenn Sie einen anderen Editor als Visual Studio oder VS Code verwenden, befolgen Sie einfach die Schritte für die Eingabeaufforderung.

### <a name="visual-studio-code-or-command-prompt"></a>[Visual Studio Code oder Eingabeaufforderung](#tab/tabid-cmdline)

- Erstellen Sie eine neue Q#-Bibliothek.

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

### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

- Erstellen Sie eine neue Q#-Bibliothek.
  - Klicken Sie auf **Datei** -> **Neu** -> **Projekt**.
  - Geben Sie „Q#“ in das Suchfeld ein.
  - Wählen Sie **Q#-Bibliothek** aus.
  - Wählen Sie **Weiter** aus.
  - Wählen Sie einen Namen und Speicherort für Ihre Bibliothek aus.
  - Stellen Sie sicher, dass die Option „Place project and solution in same directory“ (Projekt und Projektmappe im selben Verzeichnis anordnen) **deaktiviert** ist.
  - Klicken Sie auf **Erstellen**
- Erstellen eines neuen C#- oder F#-Hostprogramms
  - Navigieren Sie zu **Datei** > **Neu** > **Projekt**.
  - Wählen Sie für C# bzw. F# die Option „Konsolen-App (.NET Core)“ aus.
  - Wählen Sie **Weiter** aus.
  - Wählen Sie unter *Projektmappe* die Option „Zur Projektmappe hinzufügen“ aus.
  - Wählen Sie einen Namen für Ihr Hostprogramm aus.
  - Klicken Sie auf **Erstellen**

***

## <a name="calling-into-no-locq-from-net"></a>Durchführen von Q#-Aufrufen über .NET

Nachdem Sie Ihre Projekte gemäß der obigen Anleitung eingerichtet haben, können Sie über Ihre .NET-Konsolenanwendung Q#-Aufrufe durchführen.
Der Q#-Compiler erstellt .NET-Klassen für alle Q#-Vorgänge und -Funktionen, die das Ausführen von Quantenprogrammen in einem Simulator ermöglichen.

Das [Beispiel zur .NET-Interoperabilität](https://github.com/microsoft/Quantum/tree/main/samples/interoperability/dotnet) enthält das folgende Beispiel für einen Q#-Vorgang:

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

Um diesen Vorgang über .NET in einem Quantensimulator aufzurufen, können Sie die Methode `Run` der .NET-Klasse `RunAlgorithm` verwenden, die vom Q#-Compiler generiert wird:

### <a name="c"></a>[C#](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[F#](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie das Quantum Development Kit nun sowohl für Q#-Anwendungen als auch für die Interoperabilität mit .NET eingerichtet haben, können Sie [Ihr erstes Quantenprogramm](xref:microsoft.quantum.quickstarts.qrng) schreiben und ausführen.
