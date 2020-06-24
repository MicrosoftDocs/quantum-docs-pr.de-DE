---
title: Erstellen eines Quanten-Zufallszahlengenerators
description: Enthält eine Beschreibung der Erstellung eines Q#-Projekts, mit dem grundlegende Quantenkonzepte wie die Überlagerung veranschaulicht werden, indem ein Quanten-Zufallszahlengenerator erstellt wird.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: 18e8975e513a87c0a67a6dbb5586cc7dab5a93fb
ms.sourcegitcommit: e23178d32b316d05784a02ba3cd6166dad177e89
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2020
ms.locfileid: "84630106"
---
# <a name="tutorial-implement-a-quantum-random-number-generator-in-q"></a>Tutorial: Implementieren eines Quanten-Zufallszahlengenerators in Q\#

Ein einfaches Beispiel für einen Quantenalgorithmus, der in Q# geschrieben ist, ist ein Quanten-Zufallszahlengenerator. Für diesen Algorithmus wird das Prinzip der Quantenmechanik genutzt, um eine Zufallszahl zu generieren.

## <a name="prerequisites"></a>Voraussetzungen

- Das Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).
- Erstellen Sie ein Q#-Projekt [mithilfe von Q# über die Befehlszeile](xref:microsoft.quantum.install.standalone) oder mit einem [Python-Hostprogramm](xref:microsoft.quantum.install.python) bzw. [C#-Hostprogramm](xref:microsoft.quantum.install.cs).

## <a name="write-a-q-operation"></a>Schreiben einer Q#-Operation

### <a name="q-operation-code"></a>Q#-Operationscode

1. Ersetzen Sie den Inhalt der Datei „Program.qs“ durch den folgenden Code:

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-15,34":::

Wie im Artikel [Grundlegendes zu Quantencomputing](xref:microsoft.quantum.overview.understanding) erklärt, stellt ein Qubit eine Einheit mit Quanteninformationen dar, die sich in einem Superpositionszustand befinden kann. Für ein Qubit kann sich bei einer Messung nur 0 oder 1 ergeben. Während der Ausführung steht der Zustand des Qubits aber für die Wahrscheinlichkeit, dass sich für eine Messung entweder 0 oder 1 ergibt. Dieser Wahrscheinlichkeitszustand wird als Überlagerung bezeichnet. Wir können diese Wahrscheinlichkeit verwenden, um Zufallszahlen zu generieren.

In unserer Q#-Operation führen wir den nativen Q#-Datentyp `Qubit` ein. Wir können `Qubit` nur mit einer `using`-Anweisung zuordnen. Nach der Zuordnung befindet sich ein Qubit immer im Zustand `Zero`. 

Mit der Operation `H` können wir das `Qubit` in den Zustand der Überlagerung versetzen. Zum Messen eines Qubits und Lesen seines Werts verwenden Sie die intrinsische Operation `M`.

Indem wir das `Qubit` in den Zustand der Überlagerung versetzen und die Messung durchführen, ergibt sich bei jedem Codeaufruf ein anderer Wert als Ergebnis.

Wenn die Zuordnung für ein `Qubit` aufgehoben wird, muss es explizit zurück in den Zustand `Zero` versetzt werden. Andernfalls wird vom Simulator ein Laufzeitfehler gemeldet. Eine einfache Möglichkeit, dies zu erreichen, ist das Aufrufen von `Reset`.

### <a name="visualizing-the-code-with-the-bloch-sphere"></a>Visualisieren des Codes mit der Bloch-Kugel

Bei der Bloch-Kugel steht der Nordpol für den klassischen Wert **0** und der Südpol für den klassischen Wert **1**. Jede Überlagerung kann durch einen Punkt auf der Kugel dargestellt werden (per Pfeil). Je näher sich das Ende des Pfeils an einem der Pole befindet, desto höher ist die Wahrscheinlichkeit, dass das Qubit bei einer Messung auf den klassischen Wert zurückfällt, der dem Pol zugeordnet ist. Der unten durch den roten Pfeil dargestellte Qubit-Zustand verfügt beispielsweise über eine höhere Wahrscheinlichkeit, dass sich bei einer Messung der Wert **0** ergibt.

<img src="~/media/qrng-Bloch.png" width="175" alt="A qubit state with a high probability of measuring zero">

Wir können diese Darstellung verwenden, um die Aktivitäten des Codes zu visualisieren:

* Wir beginnen mit einem im Zustand **0** initialisierten Qubit und wenden `H` an, um eine Überlagerung zu erstellen, bei der die Wahrscheinlichkeiten für **0** und **1** gleich hoch sind.

<img src="~/media/qrng-H.png" width="450" alt="Preparing a qubit in superposition">

* Anschließend messen wir das Qubit und speichern die Ausgabe:

<img src="~/media/qrng-meas.png" width="450" alt="Measuring a qubit and saving the output">

Da das Ergebnis der Messung völlig zufällig ist, erhalten wir ein zufälliges Bit. Wir können diesen Vorgang mehrmals aufrufen, um ganze Zahlen zu erstellen. Wenn wir den Vorgang beispielsweise dreimal aufrufen, um drei zufällige Bits zu erhalten, können wir zufällige 3-Bit-Zahlen erstellen (also eine Zufallszahl zwischen 0 und 7).


## <a name="creating-a-complete-random-number-generator"></a>Erstellen eines vollständigen Zufallszahlengenerators

Sie besitzen nun einen Q#-Vorgang, der zufällige Bits generiert, und können damit einen vollständigen Quanten-Zufallszahlengenerator erstellen. Sie können die Q#-Befehlszeilenanwendungen oder ein Hostprogramm verwenden.



### <a name="q-command-line-applications-with-visual-studio-or-visual-studio-code"></a>[Q#-Befehlszeilenanwendungen mit Visual Studio oder Visual Studio Code](#tab/tabid-qsharp)

Fügen Sie zum Erstellen der vollständigen Q#-Befehlszeilenanwendung Ihrem Q#-Programm den folgenden Einstiegspunkt hinzu: 

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="17-33":::

Die ausführbare Datei führt den Vorgang oder die Funktion, der bzw. die mit dem Attribut `@EntryPoint()` markiert ist, abhängig von der Projektkonfiguration und den Befehlszeilenoptionen für einen Simulator oder eine Ressourcenschätzung aus.

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-34":::

Drücken Sie in Visual Studio einfach STRG+F5, um das Skript auszuführen.

Erstellen Sie in VS Code erstmalig die Datei „Program.qs“, indem Sie Folgendes im Terminal eingeben:

```dotnetcli
dotnet build
```

Bei nachfolgenden Ausführungen muss diese Datei nicht erneut erstellt werden. Geben Sie für die Ausführung den folgenden Befehl ein, und drücken Sie die EINGABETASTE:

```dotnetcli
dotnet run --no-build
```

### <a name="python-with-visual-studio-code-or-the-command-line"></a>[Python mit Visual Studio Code oder Befehlszeile](#tab/tabid-python)

Um Ihr neues Q#-Programm aus Python auszuführen, speichern Sie den folgenden Code als `host.py`:

:::code language="python" source="~/quantum/samples/interoperability/qrng/host.py" range="11-30":::

Anschließend können Sie Ihr Python-Hostprogramm an der Befehlszeile ausführen:

```bash
$ python host.py
Preparing Q# environment...
..The random number generated is 42
```

### <a name="c-with-visual-studio-code-or-visual-studio"></a>[C# mit Visual Studio Code oder Visual Studio](#tab/tabid-csharp)

Um Ihr neues Q#-Programm aus C# auszuführen, ändern Sie `Driver.cs`, so dass es den folgenden C#-Code beinhaltet:

:::code language="csharp" source="~/quantum/samples/interoperability/qrng/Host.cs" range="4-39":::

Anschließend können Sie Ihr C#-Hostprogramm über die Befehlszeile ausführen (drücken Sie in Visual Studio F5):

```bash
$ dotnet run
The random number generated is 42
```

***
