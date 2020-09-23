---
title: Einrichten des Microsoft Quantum Development Kit (QDK)
description: Hier erfahren Sie, wie Sie das Microsoft Quantum Development Kit (QDK) für verschiedene Umgebungen einrichten.
author: bradben
ms.author: v-benbra
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 74b9b3d8f694072f5b5f4d0eb520263387de8919
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834481"
---
# <a name="setting-up-the-microsoft-quantum-development-kit-qdk"></a>Einrichten des Microsoft Quantum Development Kit (QDK)

Hier erfahren Sie, wie Sie das Microsoft Quantum Development Kit (QDK) für Ihre Umgebung einrichten, um mit der Quantenprogrammierung beginnen zu können. Das QDK umfasst Folgendes:

- Die Programmiersprache Q#
- Bibliotheken zur Abstraktion komplexer Funktionen in Q#
- API für die Sprachen Python und .NET (C#, F# und VB.NET) zum Ausführen von Quantenprogrammen, die in Q# geschrieben sind
- Tools für die Entwicklung

Q#-Programme können als eigenständige Anwendungen unter Verwendung von Visual Studio Code oder Visual Studio oder über Jupyter Notebook-Instanzen mit dem IQ#-Jupyter-Kernel ausgeführt werden. Alternativ können sie mit einem in Python oder in einer .NET-Sprache (C#, F#) geschriebenen Hostprogramm kombiniert werden. Darüber hinaus können Sie Q#-Programme auch online unter Verwendung von [Codespaces](https://online.visualstudio.com/), [MyBinder.org](https://mybinder.org/) oder [Docker](#use-the-qdk-with-docker) ausführen. 

## <a name="options-for-setting-up-the-qdk"></a>Optionen für die QDK-Einrichtung

Das QDK kann auf drei Arten verwendet werden:

- [Lokales Installieren des QDK](#install-the-qdk-locally)
- [Verwenden des QDK online](#use-the-qdk-online)
- [Verwenden eines QDK-Docker-Images](#use-the-qdk-with-docker)

## <a name="install-the-qdk-locally"></a>Lokales Installieren des QDK

Sie können Q#-Code in den meisten gängigen IDEs entwickeln und Q# in andere Sprachen wie Python und .NET (C#, F#) integrieren.

|&nbsp; | **VS Code<br>(ab 2019)**| **Visual Studio<br>(ab 2019)** | **Jupyter-Notebooks** | **Befehlszeile**|
|:-----|:-----:|:-----:|:-----:|:-----:|
|**Betriebssystem** |Windows, macOS, Linux |Nur Windows |Windows, macOS, Linux |Windows, macOS, Linux |
|<br>**Q# (eigenständig)** |<br>[Installieren](xref:microsoft.quantum.install.standalone) |<br> [Installieren](xref:microsoft.quantum.install.standalone)  |<br> [Installieren](xref:microsoft.quantum.install.jupyter) |<br>[Installieren](xref:microsoft.quantum.install.standalone)|
|**Q# und Python** |[Installieren](xref:microsoft.quantum.install.python) |[Installieren](xref:microsoft.quantum.install.python) |[Installieren](xref:microsoft.quantum.install.jupyter) |[Installieren](xref:microsoft.quantum.install.python) |
|**Q# und .NET (C#, F#)**|[Installieren](xref:microsoft.quantum.install.cs) |[Installieren](xref:microsoft.quantum.install.cs)|&#10006; |[Installieren](xref:microsoft.quantum.install.cs) |

## <a name="use-the-qdk-online"></a>Verwenden des QDK online

Die Entwicklung von Q#-Code ist auch ganz ohne lokale Installation möglich. Hierzu stehen folgende Optionen zur Verfügung:

|Resource|Vorteile|Einschränkungen|
|---|---|---|
|[**Visual Studio Codespaces**](xref:microsoft.quantum.install.standalone)|Umfangreiche Onlineentwicklungsumgebung  |Azure-Abonnement und entsprechender Tarif erforderlich |
|[**Binder**](xref:microsoft.quantum.install.binder) | Kostenlose onlinebasierte Notebookumgebung |Keine Persistenz |

## <a name="use-the-qdk-with-docker"></a>Verwenden des QDK mit Docker

Sie können unser QDK-Docker-Image in Ihrer lokalen Docker-Installation oder in der Cloud über einen beliebigen Dienst nutzen, der Docker-Images unterstützt. Ein Beispiel wäre etwa ACI.

Das IQ#-Docker-Image steht unter https://github.com/microsoft/iqsharp/#using-iq-as-a-container zum Download bereit. 

Docker kann auch mit einem Visual Studio Code-Remoteentwicklungscontainer verwendet werden, um schnell Entwicklungsumgebungen zu definieren. Weitere Informationen zu VS Code-Entwicklungscontainern finden Sie unter https://github.com/microsoft/Quantum/tree/master/.devcontainer.

## <a name="next-steps"></a>Nächste Schritte

Die Workflows für jede dieser Einrichtungen werden in [Möglichkeiten zum Ausführen eines Q#-Programms](xref:microsoft.quantum.guide.host-programs) beschrieben und verglichen.
