---
title: Einfache Klassifizierung mit der Quantum-Machine Learning Bibliothek
description: 'Erfahren Sie, wie Sie mithilfe der Quantum-Machine Learning Bibliothek von Microsoft QDK einen in Q # geschriebenen Quantum-Klassifizierer ausführen.'
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.basics
ms.openlocfilehash: 1d2538fd164c4c61c2712978d3b5c57b0eb766e6
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275036"
---
# <a name="basic-classification-classify-data-with-the-qdk"></a>Basic-Klassifizierung: klassifizieren von Daten mit dem QDK

In dieser Schnellstartanleitung erfahren Sie, wie Sie mithilfe der Quantum-Machine Learning Bibliothek des QDK einen in Q # geschriebenen quantesequenziellen Klassifizierer ausführen. 

In dieser Anleitung verwenden wir das Halbmond-DataSet mit einer in Q # definierten Klassifizierungs Struktur.

## <a name="prerequisites"></a>Voraussetzungen

- Das Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).
- Erstellen Sie ein Q #-Projekt für ein [python-Host Programm](xref:microsoft.quantum.install.python) oder ein [c#-Host Programm](xref:microsoft.quantum.install.cs).

## <a name="host-program"></a>Host Programm

Ihr Host Programm besteht aus drei Teilen:

- Laden Sie das DataSet, und wählen Sie einen Satz von Start Parametern für das Modell aus.
- Führen Sie Schulungen aus, um die Parameter und die Verschiebung des Modells zu bestimmen.
- Überprüfen des Modells zur Bestimmung der Genauigkeit

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Python mit Visual Studio Code oder Befehlszeile](#tab/tabid-python)

    Wenn Sie den Q #-Klassifizierer aus python ausführen möchten, speichern Sie den folgenden Code als `host.py` . Beachten Sie, dass Sie auch die Q #-Datei benötigen `Training.qs` , die später in diesem Tutorial erläutert wird.

    :::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="3-42":::

    Anschließend können Sie Ihr Python-Hostprogramm an der Befehlszeile ausführen:

    ```bash
    $ python host.py
    Preparing Q# environment...
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[C# mit Visual Studio Code oder Befehlszeile](#tab/tabid-csharp)

    Wenn Sie den Q #-Klassifizierer aus c# ausführen möchten, speichern Sie den folgenden Code als `Host.cs` . Beachten Sie, dass Sie auch die Q #-Datei benötigen `Training.qs` , die später in diesem Tutorial erläutert wird.

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    Anschließend können Sie Ihr C#-Hostprogramm an der Befehlszeile ausführen:

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-2019"></a>[C# mit Visual Studio 2019](#tab/tabid-vs2019)

    Um das neue Q #-Programm aus c# in Visual Studio auszuführen, ändern `Host.cs` Sie, um den folgenden c#-Code einzufügen. Beachten Sie, dass Sie auch die Q #-Datei benötigen `Training.qs` , die später in diesem Tutorial erläutert wird.

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    Drücken Sie dann F5. Das Programm wird gestartet, und ein neues Fenster mit den folgenden Ergebnissen wird angezeigt: 

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```
    ***

## <a name="q-classifier-code"></a>Q- \# Klassifizierungs Code

Sehen wir uns nun an, wie die vom Host Programm aufgerufenen Vorgänge in f # definiert werden.
Der folgende Code wird in einer Datei mit dem Namen gespeichert `Training.qs` .

:::code language="qsharp" source="~/quantum/samples/machine-learning/half-moons/Training.qs" range="4-116":::

Die wichtigsten im obigen Code definierten Funktionen und Vorgänge sind:

- `ClassifierStructure() : ControlledRotation[]`: in dieser Funktion legen wir die Struktur unseres Verbindungs Modells fest, indem wir die Ebenen der kontrollierten Gates hinzufügen, die wir in Erwägung gezogen haben. Dieser Schritt entspricht der Deklaration von Neuronen-Ebenen in einem sequenziellen Deep Learning-Modell.
- `TrainHalfMoonModel() : (Double[], Double)`: dieser Vorgang ist der Kernteil des Codes und definiert das Training. Hier laden wir die Beispiele aus dem DataSet, das in der Bibliothek enthalten ist, legen die Hyperparameter und die ursprünglichen Parameter für das Training fest und beginnen mit dem Training, indem wir den `TrainSequentialClassifier` in der Bibliothek enthaltenen Vorgang aufrufen. Es gibt die Parameter und die Verschiebung aus, die den Klassifizierer bestimmen.
- `ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int`: dieser Vorgang definiert den Validierungsprozess zum Auswerten des Modells. Hier laden wir die Beispiele für die Überprüfung, die Anzahl der Messungen pro Stichprobe und die Toleranz. Er gibt die Anzahl der fehl Klassifizierungen für den ausgewählten Batch von Beispielen für die Validierung aus.

## <a name="next-steps"></a>Nächste Schritte

Zuerst können Sie mit dem Code experimentieren und versuchen, einige Parameter zu ändern, um zu sehen, wie sich dies auf das Training auswirkt. Im nächsten Tutorial entwerfen Sie dann [ihren eigenen Klassifizierer](xref:microsoft.quantum.libraries.machine-learning.design). Sie erfahren, wie Sie die Struktur des Klassifizierers definieren.
