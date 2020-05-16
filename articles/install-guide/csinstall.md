---
title: Entwickeln mit Q# und .Net
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install.cs
ms.openlocfilehash: 155367dbb1373f00e2b0bd732a5319b32462c9f9
ms.sourcegitcommit: 2317473fdf2b80de58db0f43b9fcfb57f56aefff
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2020
ms.locfileid: "83426499"
---
# <a name="develop-with-q-and-net"></a>Entwickeln mit Q# und .Net

F # ist für .NET-Sprachen wie c# und F # konzipiert.
In dieser Anleitung erfahren Sie, wie Sie Q # mit einem in einer .NET-Sprache geschriebenen Host Programm verwenden.

## <a name="prerequisites"></a>Voraussetzungen

- Installieren Sie das Quantum Development Kit [für die Verwendung mit f #-Befehlszeilen Projekten](xref:microsoft.quantum.install.standalone).

## <a name="creating-a-q-library-and-a-net-host"></a>Erstellen einer Q #-Bibliothek und eines .NET-Hosts

Der erste Schritt besteht im Erstellen von Projekten für die q #-Bibliothek und für den .NET-Host, der die in der q #-Bibliothek definierten Vorgänge und Funktionen aufruft.

### <a name="visual-studio-2019"></a>[Visual Studio 2019](#tab/tabid-vs2019)

- Erstellen einer neuen Q #-Bibliothek
  - Wechseln Sie zu **Datei**  ->  **Neues**  ->  **Projekt** .
  - Geben Sie "Q #" in das Suchfeld ein.
  - **Q #-Bibliothek** auswählen
  - Klicken Sie auf **Weiter**.
  - Auswählen eines Namens und eines Speicher Orts für die Bibliothek
  - Stellen Sie sicher, dass "Projekt und Projekt Mappe in demselben Verzeichnis platzieren" nicht **aktiviert** ist.
  - Klicken Sie auf **Erstellen**.
- Erstellen eines neuen c#-oder F #-Host Programms
  - Gehe zu **Datei** → **neu** → **Projekt**
  - Wählen Sie "Konsolen-app (.net Core") "für c# oder F aus. #
  - Klicken Sie auf **Weiter**.
  - Wählen *Sie Unterprojekt*Mappe die Option zur Projekt Mappe hinzufügen aus.
  - Wählen Sie einen Namen für das Host Programm aus.
  - Klicken Sie auf **Erstellen**.

### <a name="visual-studio-code-or-command-line"></a>[Visual Studio Code oder Befehlszeile](#tab/tabid-cmdline)

- Erstellen einer neuen Q #-Bibliothek

  ```dotnetcli
  dotnet new classlib -lang Q# -o quantum
  ```

- Neues c#-oder F #-Konsolen Projekt erstellen

  ```dotnetcli
  dotnet new console -lang C# -o host  
  ```

- Hinzufügen der Q #-Bibliothek als Verweis von Ihrem Host Programm

  ```dotnetcli
  cd host
  dotnet add reference ../quantum/quantum.csproj
  ```

- Optionale Erstellen einer Projekt Mappe für beide Projekte

  ```dotnetcli
  dotnet new sln -n quantum-dotnet
  dotnet sln quantum-dotnet.sln add ./quantum/quantum.csproj
  dotnet sln quantum-dotnet.sln add ./host/host.csproj
  ```

***

## <a name="calling-into-q-from-net"></a>Aufrufen von f # aus .net

Nachdem Sie Ihre Projekte gemäß den obigen Anweisungen eingerichtet haben, können Sie in der .NET-Konsolenanwendung Q # anrufen.
Der f #-Compiler erstellt .NET-Klassen für jeden q #-Vorgang und jede Funktion, die es Ihnen ermöglichen, die Quantum-Programme in einem Simulator auszuführen.

Beispielsweise enthält das [.net-Interoperabilitäts](https://github.com/microsoft/Quantum/tree/master/samples/interoperability/dotnet) Beispiel das folgende Beispiel für einen Q #-Vorgang:

:::code language="qsharp" source="~/quantum/samples/interoperability/dotnet/qsharp/Operations.qs" range="67-75":::

Um diesen Vorgang von .net in einem Quantum-Simulator aufzurufen, können Sie die- `Run` Methode der .NET-Klasse verwenden, die `RunAlgorithm` vom Q #-Compiler generiert wird:

### <a name="c"></a>[C#](#tab/tabid-csharp)

:::code language="csharp" source="~/quantum/samples/interoperability/dotnet/csharp/Host.cs" range="4-":::

### <a name="f"></a>[F#](#tab/tabid-fsharp)

:::code language="fsharp" source="~/quantum/samples/interoperability/dotnet/fsharp/Host.fs" range="4-":::

***
    
## <a name="next-steps"></a>Nächste Schritte

Nun, da Sie das Quantum Development Kit sowohl für Q #-Befehlszeilen Programme als auch für die Interoperabilität mit .net eingerichtet haben, können Sie [Ihr erstes Quantum-Programm](xref:microsoft.quantum.quickstarts.qrng)schreiben und ausführen.
