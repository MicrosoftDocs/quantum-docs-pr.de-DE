---
title: Einrichten des Microsoft Quantum Development Kit (QDK)
description: Hier erfahren Sie, wie Sie das Microsoft Quantum Development Kit (QDK) für verschiedene Umgebungen einrichten.
author: bradben
ms.author: v-benbra
ms.date: 5/8/2020
ms.topic: quickstart
uid: microsoft.quantum.install
no-loc:
- Q#
- $$v
ms.openlocfilehash: 15067f1762f4468345beee38c98e1b943081fc1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859023"
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

<table>
    <tr>
        <th width=10%>&nbsp;</th>
        <th>&nbsp;</th>
        <th align="center" width=18%><img src="~/media/vs_code.png" alt="VS Code" width="50"/><br><b>VS-Code<br>(2019 oder höher)</b></th>
        <th align="center" width=18%><img src="~/media/vs_studio.png" alt="Visual Studio" width="50"/><br><b>Visual Studio<br>(2019 oder höher)</b></th>
        <th align="center" width=18%><img src="~/media/jupyter-wht.png" alt="jupyter install" width="65"/><br><b>Jupyter-Notebooks</b></th>
        <th align="center" width=18%><img src="~/media/blank.png" alt="blank spacer" width="65"/><br><b>Befehlszeile</b></th>
    </tr>
    <tr>
        <th>&nbsp;</th>
        <td align="left"><b>Betriebssystemunterstützung :</b></td>
        <td align="center">Windows, macOS, Linux</td>
        <td align="center">Nur Windows</td>
        <td align="center">Windows, macOS, Linux</td>
        <td align="center">Windows, macOS, Linux</td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/quantum-wht.png" alt="QDK" width="60"/></td>
        <td align="left"><b>Q# (eigenständig)</b></td>
        <td align="center"><a href="xref:microsoft.quantum.install.standalone">Installieren</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.standalone">Installieren</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.jupyter">Installieren</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.standalone">Installieren</a></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/python.png" alt="python install" width="50"/></td>
        <td align="left"><b>Q# und Python</b></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Installieren</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Installieren</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Installieren</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.python">Installieren</a></td>
    </tr>
    <tr>
        <td align="right"><img src="~/media/dot_net.png" alt="dotnet install" width="50"/></td>
        <td align="left"><b>Q# und .NET (C#, F#)</b></td> 
        <td align="center"><a href="xref:microsoft.quantum.install.cs">Installieren</a></td>
        <td align="center"><a href="xref:microsoft.quantum.install.cs">Installieren</a></td>
        <td align="center">&#10006;</td>
        <td align="center"><a href="xref:microsoft.quantum.install.cs">Installieren</a></td>
   </tr>
</table>

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
