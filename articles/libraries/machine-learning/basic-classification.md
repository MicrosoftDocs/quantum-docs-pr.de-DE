---
title: Einfache Klassifizierung mit der Quantum-Machine Learning Bibliothek
description: 'Erfahren Sie, wie Sie mithilfe der Quantum-Machine Learning Bibliothek von Microsoft QDK einen in Q # geschriebenen Quantum-Klassifizierer ausführen.'
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/16/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.basics
ms.openlocfilehash: f42e3e4492f934d7a8f03d4fec6fa0de765401d7
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77909924"
---
# <a name="basic-classification-classify-data-with-the-qdk"></a>Basic-Klassifizierung: klassifizieren von Daten mit dem QDK

In dieser Schnellstartanleitung erfahren Sie, wie Sie mithilfe der Quantum-Machine Learning Bibliothek des QDK einen in Q # geschriebenen quantesequenziellen Klassifizierer ausführen. 

In dieser Anleitung verwenden wir das Halbmond-DataSet mit einer in Q # definierten Klassifizierungs Struktur.

## <a name="prerequisites"></a>Voraussetzungen

- Das Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).
- [Erstellen eines Q#-Projekts](xref:microsoft.quantum.howto.createproject)

## <a name="host-program"></a>Host Programm

Ihr Host Programm besteht aus drei Teilen:

- Laden Sie das DataSet, und wählen Sie einen Satz von Start Parametern für das Modell aus.
- Führen Sie Schulungen aus, um die Parameter und die Verschiebung des Modells zu bestimmen.
- Überprüfen des Modells zur Bestimmung der Genauigkeit

    ### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Python mit Visual Studio Code oder Befehlszeile](#tab/tabid-python)

    Wenn Sie den Q #-Klassifizierer aus python ausführen möchten, speichern Sie den folgenden Code als `host.py`. Beachten Sie, dass Sie auch das Q #-Datei `Training.qs` benötigen, das weiter unten in diesem Tutorial erläutert wird.

    :::code language="python" source="~/quantum/samples/machine-learning/half-moons/host.py" range="3-42":::

    Anschließend können Sie Ihr Python-Hostprogramm an der Befehlszeile ausführen:

    ```bash
    $ python host.py
    Preparing Q# environment...
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-code-or-the-command-line"></a>[C# mit Visual Studio Code oder Befehlszeile](#tab/tabid-csharp)

    Wenn Sie den Q #-Klassifizierer ausführen C#möchten, speichern Sie den folgenden Code als `Host.cs`. Beachten Sie, dass Sie auch das Q #-Datei `Training.qs` benötigen, das weiter unten in diesem Tutorial erläutert wird.

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    Anschließend können Sie Ihr C#-Hostprogramm an der Befehlszeile ausführen:

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```

    ### <a name="c-with-visual-studio-2019"></a>[C# mit Visual Studio 2019](#tab/tabid-vs2019)

    Um das neue Q #-Programm C# in Visual Studio auszuführen, ändern Sie `Host.cs`, um den C# folgenden Code einzufügen. Beachten Sie, dass Sie auch das Q #-Datei `Training.qs` benötigen, das weiter unten in diesem Tutorial erläutert wird.

    :::code language="csharp" source="~/quantum/samples/machine-learning/half-moons/Host.cs" range="4-86":::

    Drücken Sie dann F5. Das Programm wird gestartet, und ein neues Fenster mit den folgenden Ergebnissen wird angezeigt: 

    ```bash
    $ dotnet run
    [...]
    Observed X.XX% misclassifications.
    ```
    ***

## <a name="q-classifier-code"></a>F\# klassifizierercode

Sehen wir uns nun an, wie die vom Host Programm aufgerufenen Vorgänge in f # definiert werden.
Der folgende Code wird in einer Datei mit dem Namen `Training.qs`gespeichert.

:::code language="qsharp" source="~/quantum/samples/machine-learning/half-moons/Training.qs" range="4-116":::

Die wichtigsten im obigen Code definierten Funktionen und Vorgänge sind:

- `ClassifierStructure() : ControlledRotation[]`: in dieser Funktion wird die Struktur unseres Verbindungs Modells durch Hinzufügen der Ebenen der kontrollierten Gates festgelegt, die berücksichtigt werden. Dieser Schritt entspricht der Deklaration von Neuronen-Ebenen in einem sequenziellen Deep Learning-Modell.
- `TrainHalfMoonModel() : TrainWineModel() : (Double[], Double)`: dieser Vorgang ist der Kernteil des Codes und definiert das Training. Hier laden wir die Beispiele aus dem DataSet, das in der Bibliothek enthalten ist, legen die Hyperparameter und die ursprünglichen Parameter für das Training fest und beginnen mit dem Training, indem wir den in der Bibliothek enthaltenen Vorgang `TrainSequentialClassifier` aufrufen. Es gibt die Parameter und die Verschiebung aus, die den Klassifizierer bestimmen.
- `ValidateHalfMoonModel(parameters : Double[], bias : Double) : Int`: dieser Vorgang definiert den Validierungsprozess zum Auswerten des Modells. Hier laden wir die Beispiele für die Überprüfung, die Anzahl der Messungen pro Stichprobe und die Toleranz. Er gibt die Anzahl der fehl Klassifizierungen für den ausgewählten Batch von Beispielen für die Validierung aus.

## <a name="next-steps"></a>Nächste Schritte

Zuerst können Sie mit dem Code experimentieren und versuchen, einige Parameter zu ändern, um zu sehen, wie sich dies auf das Training auswirkt. Im nächsten Tutorial entwerfen Sie dann [ihren eigenen Klassifizierer](xref:microsoft.quantum.libraries.machine-learning.design). Sie erfahren, wie Sie die Struktur des Klassifizierers definieren.
