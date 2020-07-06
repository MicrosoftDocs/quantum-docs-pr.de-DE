---
title: Installieren des Microsoft Quantum Development Kit (QDK)
description: Hier erfahren Sie, wie Sie das Microsoft Quantum Development Kit (QDK) für verschiedene Umgebungen installieren.
author: bradben
ms.author: bradben
ms.date: 5/8/2020
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: ee8d210d67a20cfea3bdc36162efc47f021a6dc6
ms.sourcegitcommit: a3775921db1dc5c653c97b8fa8fe2c0ddd5261ff
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2020
ms.locfileid: "85885473"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>Installieren des Microsoft Quantum Development Kit (QDK)

Es wird beschrieben, wie Sie das Microsoft Quantum Development Kit (QDK) installieren, damit Sie mit der Quantenprogrammierung starten können. Das QDK umfasst Folgendes:

- Programmiersprache Q#
- Bibliotheken zur Abstraktion komplexer Funktionen in Q#
- API für die Sprachen Python und .NET (C#, F# und VB.NET) zum Ausführen von Quantenprogrammen, die in Q# geschrieben sind
- Tools für die Entwicklung

Q#-Programme können als eigenständige Anwendungen unter Verwendung von Visual Studio Code oder Visual Studio oder über Jupyter Notebook-Instanzen mit dem IQ#-Jupyter-Kernel ausgeführt werden.
Darüber hinaus können sie mit einem in einer .NET-Sprache (in der Regel C#) oder in Python geschriebenen Hostprogramm kombiniert werden, um das Aufrufen von Quantenvorgängen in einem klassischen Programm zu ermöglichen.

Die Workflows für jede dieser Einrichtungen werden in [Möglichkeiten zum Ausführen eines Q#-Programms](xref:microsoft.quantum.guide.host-programs) beschrieben und verglichen.

Wählen Sie Ihre bevorzugte Einrichtung aus, um mit der Installation des QDK und der Erstellung von Q#-Projekten fortzufahren:

[Entwickeln mit Q#-Befehlszeilenanwendungen:](xref:microsoft.quantum.install.standalone) Verwenden Sie diesen Ansatz, wenn Sie Q# über die Befehlszeile nutzen möchten. Dies erfordert im Gegensatz zu den folgenden Optionen keinen Treiber und kein Hostprogramm.

[Entwickeln mit Q#-Jupyter Notebook-Instanzen:](xref:microsoft.quantum.install.jupyter) Verwenden Sie diese Umgebung, um Q#-Code in Zellen mit eingebettetem Text auszuführen oder interaktive Tutorials zum Thema Quantencomputing zu erstellen. 

[Entwickeln mit Q# und Python:](xref:microsoft.quantum.install.python) Verwenden Sie diese Option, wenn Sie Python und Q# miteinander kombinieren möchten, um ein Python-Hostprogramm mit Aufrufen von Q#-Vorgängen zu erstellen.

[Entwickeln mit Q# und .NET:](xref:microsoft.quantum.install.cs) Kombinieren Sie C#, F# oder VB.NET mit Q#, um ein .NET-Hostprogramm mit Aufrufen von Q#-Vorgängen zu erstellen.
