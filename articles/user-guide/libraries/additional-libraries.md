---
title: 'Verwenden zusätzlicher Q #-Bibliotheken'
description: 'Erfahren Sie, wie Sie Ihren Quantum-Anwendungen weitere Q #-Bibliotheken hinzufügen.'
author: cgranade
ms.author: chgranad
ms.date: 06/30/2020
ms.topic: article
uid: microsoft.quantum.libraries.using
ms.openlocfilehash: b82113b925870d07c8a28aecd50176e009826062
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86872621"
---
# <a name="using-additional-q-libraries"></a>Verwenden zusätzlicher Q #-Bibliotheken

Das Quantum Development Kit bietet zusätzliche domänenspezifische Funktionen über _nuget-Pakete_ , die zu Ihren Q #-Projekten hinzugefügt werden können.

| Q #-Bibliothek  | NuGet-Paket | Hinweise |
|---------|---------|--------|
| [F #-Standardbibliothek](xref:microsoft.quantum.libraries.standard.intro) | [**Microsoft. Quantum. Standard**](https://www.nuget.org/packages/Microsoft.Quantum.Standard) | Standardmäßig inbegriffen |
| [Quantenchemiebibliothek](xref:microsoft.quantum.chemistry.concepts.intro) | [**Microsoft.Quantum.Chemistry**](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) | |
| [Numerische Quantenbibliothek](xref:microsoft.quantum.numerics.intro) | [**Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) | |
| [Quantum Machine Learning-Bibliothek](xref:microsoft.quantum.libraries.machine-learning.intro) | [**Microsoft.Quantum.MachineLearning**](https://www.nuget.org/packages/Microsoft.Quantum.MachineLearning) | |

Nachdem Sie das Quantum Development Kit zur Verwendung mit Ihrer bevorzugten Umgebung und Host Sprache installiert haben, können Sie ohne weitere Installation Bibliotheken problemlos einzelnen Q #-Projekten hinzufügen.

> [!NOTE]
> Einige q #-Bibliotheken funktionieren möglicherweise gut mit zusätzlichen Tools, die zusammen mit den q #-Programmen verwendet werden oder in Ihre Host Anwendungen integriert werden können.
> Beispielsweise wird in den [Installationsanweisungen für die Chemie Bibliothek](xref:microsoft.quantum.chemistry.concepts.installation) beschrieben, wie Sie das [ **Microsoft. Quantum. Chemistry** -Paket](https://www.nuget.org/packages/Microsoft.Quantum.Chemistry) zusammen mit der nwchem-computegrafieplattform verwenden und wie Sie die `qdk-chem` Befehlszeilen Tools zum Arbeiten mit Quantum-Chemie-Daten installieren.

## <a name="q-command-line-applications-or-net-interopability"></a>[F #-Befehlszeilen Anwendungen oder .NET-Interoperabilität](#tab/tabid-csproj)

**Befehlszeile oder Visual Studio Code:** Mithilfe der Befehlszeile eigenständig oder innerhalb Visual Studio Code können Sie dem `dotnet` Projekt einen nuget-Paket Verweis hinzufügen.
Wenn Sie z [**. b. das Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) -Paket hinzufügen möchten, führen Sie den folgenden Befehl aus:

```dotnetcli
dotnet add package Microsoft.Quantum.Numerics
```

**Visual Studio:** Wenn Sie Visual Studio 2019 oder höher verwenden, können Sie mit dem nuget-Paket-Manager weitere Q #-Pakete hinzufügen.
So laden Sie ein Paket: 
1. Wenn ein Projekt in Visual Studio geöffnet ist, wählen Sie im Menü **Projekt** die Option **nuget-Pakete verwalten...** aus.

2. Klicken Sie auf **Durchsuchen**, wählen Sie **Vorabversion einschließen** aus, und suchen Sie nach dem Paketnamen "Microsoft. Quantum. Numerics". Dadurch werden die Pakete aufgelistet, die zum Herunterladen zur Verfügung stehen.

3. Zeigen Sie auf **Microsoft. Quantum. Numerics** , und klicken Sie auf den nach unten zeigenden Pfeil rechts neben der Versionsnummer, um das Numerics-Paket zu installieren.

Weitere Informationen finden Sie im Leitfaden für die [Benutzeroberfläche des Paket-Managers](https://docs.microsoft.com/nuget/tools/package-manager-ui).

Alternativ können Sie die Numerics-Bibliothek mithilfe der Paket-Manager-Konsole über die Befehlszeilenschnittstelle dem Projekt hinzufügen.

![Verwenden der Paket-Manager-Konsole über die Befehlszeile](~/media/vs2017-nuget-console-menu.png)

Führen Sie in der Paket-Manager-Konsole Folgendes aus:

```
Install-Package Microsoft.Quantum.Numerics
```

Weitere Informationen finden Sie im Handbuch für die [Paket-Manager-Konsole](https://docs.microsoft.com/nuget/tools/package-manager-console).

## <a name="iq-notebooks"></a>[IQ # Notebooks](#tab/tabid-notebook)

Mithilfe des [ `%package` Magic-Befehls](xref:microsoft.quantum.iqsharp.magic-ref.package)können Sie zusätzliche Pakete zur Verwendung in einem IQ # Notebook verfügbar machen.
Um z. b. das [**Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) -Paket für die Verwendung in einem IQ # Notebook hinzuzufügen, führen Sie den folgenden Befehl in einer Notebook-Zelle aus:

```
%package Microsoft.Quantum.Numerics
```

Nach diesem Befehl ist das Paket für alle Zellen im Notebook verfügbar.
Um das Paket über den Q #-Code im aktuellen Arbeitsbereich verfügbar zu machen, laden Sie den Arbeitsbereich nach dem Hinzufügen des Pakets neu:

```
%workspace reload
```

## <a name="python-interoperability"></a>[Interoperabilität mit Python](#tab/tabid-python)


Mithilfe der-Methode können Sie zusätzliche Pakete zur Verwendung in einem python-Host Programm verfügbar machen [`qsharp.packages.add`](https://docs.microsoft.com/python/qsharp/qsharp.packages.packages) .
Um z. b. das [**Microsoft. Quantum. Numerics**](https://www.nuget.org/packages/Microsoft.Quantum.Numerics) -Paket für die Verwendung in einem IQ # Notebook hinzuzufügen, führen Sie den folgenden Python-Code aus:

```python
import qsharp
qsharp.packages.add("Microsoft.Quantum.Numerics")
```

Nach diesem Befehl wird das Paket allen mit kompilierten Q #-Code zur Verfügung gestellt `qsharp.compile` .
Um das Paket über den Q #-Code im aktuellen Arbeitsbereich verfügbar zu machen, laden Sie den Arbeitsbereich nach dem Hinzufügen des Pakets neu:

```python
qsharp.reload()
```

***
