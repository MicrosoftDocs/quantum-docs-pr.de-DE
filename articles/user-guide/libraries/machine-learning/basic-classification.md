---
title: Einfache Klassifizierung mit der Quantum-Machine Learning Bibliothek
description: Erfahren Sie, wie Sie Q# mithilfe der Quantum-Machine Learning Bibliothek von Microsoft QDK einen in geschriebenen Quantum-Klassifizierungs Klassifizierer ausführen.
author: geduardo
ms.author: v-edsanc
ms.date: 02/16/2020
ms.topic: conceptual
uid: microsoft.quantum.libraries.machine-learning.basics
no-loc:
- Q#
- $$v
ms.openlocfilehash: 4fe686a87fbdc610badc0bbcbc0bf7b065e0bce9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854041"
---
# <a name="basic-classification-classify-data-with-the-qdk"></a>Basic-Klassifizierung: klassifizieren von Daten mit dem QDK

In dieser Schnellstartanleitung erfahren Sie, wie Sie Q# mithilfe der Quantum-Machine Learning-Bibliothek des QDK einen in geschriebenen quantumziellen Klassifizierungs-Klassifizierer ausführen. 

In diesem Handbuch verwenden wir das Halbmond-DataSet, indem wir eine Klassifizierungs Struktur verwenden, die in definiert ist Q# .

## <a name="prerequisites"></a>Voraussetzungen

- Das Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).
- Erstellen Sie ein Q# Projekt für ein [python-Host Programm](xref:microsoft.quantum.install.python) oder ein [c#-Host Programm](xref:microsoft.quantum.install.cs).

## <a name="host-program"></a>Host Programm

Ihr Host Programm besteht aus drei Teilen:

- Laden Sie das DataSet, und wählen Sie einen Satz von Start Parametern für das Modell aus.
- Führen Sie Schulungen aus, um die Parameter und die Verschiebung des Modells zu bestimmen.
- Überprüfen des Modells zur Bestimmung der Genauigkeit

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Python mit Visual Studio Code oder Befehlszeile](#tab/tabid-python)

    Um die Q# Klassifizierung aus python auszuführen, speichern Sie den folgenden Code als `host.py` . Beachten Sie, dass Sie auch die Q# Datei benötigen `Training.qs` , die später in diesem Tutorial erläutert wird.

    :::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="3-42":::

    Anschließend können Sie Ihr Python-Hostprogramm an der Befehlszeile ausführen:

    ```bash
    $ python host.py
    Preparing Q# environment...
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[C# mit Visual Studio Code oder Befehlszeile](#tab/tabid-csharp)

    Um die Q# Klassifizierung aus c# auszuführen, speichern Sie den folgenden Code als `Host.cs` . Beachten Sie, dass Sie auch die Q# Datei benötigen `Training.qs` , die später in diesem Tutorial erläutert wird.

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    Anschließend können Sie Ihr C#-Hostprogramm an der Befehlszeile ausführen:

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-2019"></a>[C# mit Visual Studio 2019](#tab/tabid-vs2019)

    Um Q# das neue Programm aus c# in Visual Studio auszuführen, ändern `Host.cs` Sie, um den folgenden c#-Code einzufügen. Beachten Sie, dass Sie auch die Q# Datei benötigen `Training.qs` , die später in diesem Tutorial erläutert wird.

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    Drücken Sie F5, damit das Programm ausgeführt wird. Die folgenden Ergebnisse werden in einem neuen Fenster angezeigt: 

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```
    ***

## <a name="q-classifier-code"></a>Q- \# Klassifizierungs Code

Nun sehen wir uns an, wie die vom Host Programm aufgerufenen Vorgänge in definiert werden Q# .
Der folgende Code wird in einer Datei mit dem Namen gespeichert `Training.qs` .

:::code language="qsharp" source="~/quantum/samples/machine-learning/half-moons/Training.qs" range="4-116":::

Die wichtigsten im obigen Code definierten Funktionen und Vorgänge sind:

- `ClassifierStructure() : ControlledRotation[]` : in dieser Funktion legen wir die Struktur unseres Verbindungs Modells fest, indem wir die Ebenen der kontrollierten Gates hinzufügen, die wir in Erwägung gezogen haben. Dieser Schritt entspricht der Deklaration von Neuronen-Ebenen in einem sequenziellen Deep Learning-Modell.
- `TrainHalfMoonModel() : (Double[], Double)` : dieser Vorgang ist der Kernteil des Codes und definiert das Training. Hier laden wir die Beispiele aus dem DataSet, das in der Bibliothek enthalten ist, legen die Hyperparameter und die ursprünglichen Parameter für das Training fest und beginnen mit dem Training, indem wir den `TrainSequentialClassifier` in der Bibliothek enthaltenen Vorgang aufrufen. Es gibt die Parameter und die Verschiebung aus, die den Klassifizierer bestimmen.
- `ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int` : dieser Vorgang definiert den Validierungsprozess zum Auswerten des Modells. Hier laden wir die Beispiele für die Überprüfung, die Anzahl der Messungen pro Stichprobe und die Toleranz. Er gibt die Anzahl der fehl Klassifizierungen für den ausgewählten Batch von Beispielen für die Validierung aus.

## <a name="next-steps"></a>Nächste Schritte

Zuerst können Sie mit dem Code experimentieren und versuchen, einige Parameter zu ändern, um zu sehen, wie sich dies auf das Training auswirkt. Im nächsten Tutorial entwerfen Sie dann [ihren eigenen Klassifizierer](xref:microsoft.quantum.libraries.machine-learning.design). Sie erfahren, wie Sie die Struktur des Klassifizierers definieren.
