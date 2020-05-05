---
title: Installieren des Microsoft Quantum Development Kit (QDK)
description: Es wird beschrieben, wie Sie das Microsoft Quantum Development Kit für C#-, Python- und Jupyter Notebook-Umgebungen installieren.
author: natke
ms.author: nakersha
ms.date: 9/30/2019
ms.topic: article
ms.custom: how-to
uid: microsoft.quantum.install
ms.openlocfilehash: bca700660094b91f1c0dfa03f9bce1336073ca51
ms.sourcegitcommit: db23885adb7ff76cbf8bd1160d401a4f0471e549
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2020
ms.locfileid: "82680192"
---
# <a name="install-the-microsoft-quantum-development-kit-qdk"></a>Installieren des Microsoft Quantum Development Kit (QDK)

Es wird beschrieben, wie Sie das Microsoft Quantum Development Kit (QDK) installieren, damit Sie mit der Quantenprogrammierung starten können. Das QDK umfasst Folgendes:

- Programmiersprache Q#
- Bibliotheken zur Abstraktion komplexer Funktionen in Q#
- API für die Sprachen Python und .NET (C#, F# und VB.NET) zum Ausführen von Quantenprogrammen, die in Q# geschrieben sind
- Tools für die Entwicklung

Q#-Programme sind häufig mit einem Hostprogramm gekoppelt, das in einer .NET-Sprache (normalerweise C#) oder Python geschrieben ist. Dies ermöglicht es uns, Quantenvorgänge aus einem klassischen Programm aufzurufen.
Zusätzlich wird über das QDK die Q#-Unterstützung für Jupyter Notebooks mit dem IQ#-Jupyter-Kernel bereitgestellt.

Das QDK ist für mehrere Entwicklungsumgebungen verfügbar. Wählen Sie in den folgenden Abschnitten Ihre bevorzugte Option aus:

- [Q#-Befehlszeilenanwendung:](xref:microsoft.quantum.install.standalone) Wählen Sie diesen Ansatz, wenn Sie in der Befehlszeile mit Q# arbeiten möchten. Dies erfordert im Gegensatz zu den folgenden Optionen keinen Treiber und kein Hostprogramm.
- [Installation von Q# für Jupyter Notebooks:](xref:microsoft.quantum.install.jupyter) Wählen Sie diese Umgebung aus, um Q#-Code in Zellen mit eingebettetem Text auszuführen oder interaktive Tutorials zum Thema Quantencomputing zu erstellen. 
- [Entwickeln mit Q# und Python:](xref:microsoft.quantum.install.python) Wählen Sie diese Option, wenn Sie Python und Q# kombinieren möchten, um ein Python-Hostprogramm mit Aufrufen von Q#-Vorgängen zu erstellen.
- [Entwickeln mit Q# und C# oder F#:](xref:microsoft.quantum.install.cs) Wählen Sie diese Option, wenn Sie C# oder F# und Q# kombinieren möchten, um ein .NET-Hostprogramm mit Aufrufen von Q#-Vorgängen zu erstellen.
