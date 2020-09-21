---
title: Erstellen eines Quanten-Zufallszahlengenerators
description: Erstellen Sie ein Q# Projekt, das grundlegende Quantum-Konzepte wie Superposition veranschaulicht, indem Sie einen Quantum-Zufallszahlengenerator erstellen.
author: bromeg
ms.author: megbrow
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
no-loc:
- Q#
- $$v
ms.openlocfilehash: a0e8933e6a77d017db914e4bb969ea05f760a443
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90834039"
---
# <a name="tutorial-implement-a-quantum-random-number-generator-in-q"></a>Tutorial: Implementieren eines Quanten-Zufallszahlengenerators in Q\#

Ein einfaches Beispiel für einen in geschriebenen Quantum-Algorithmus Q# ist ein Quantum-Zufallszahlengenerator. Für diesen Algorithmus wird das Prinzip der Quantenmechanik genutzt, um eine Zufallszahl zu generieren.

## <a name="prerequisites"></a>Voraussetzungen

- Das Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).
- Erstellen Sie ein Q# Projekt für eine- [ Q# Anwendung](xref:microsoft.quantum.install.standalone), ein [python-Host Programm](xref:microsoft.quantum.install.python)oder ein [c#-Host Programm](xref:microsoft.quantum.install.cs).

## <a name="write-a-no-locq-operation"></a>Schreiben eines- Q# Vorgangs

### <a name="no-locq-operation-code"></a>Q# Vorgangs Code

1. Ersetzen Sie den Inhalt der Datei „Program.qs“ durch den folgenden Code:

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-15,34":::

Wie im Artikel [Grundlegendes zu Quantencomputing](xref:microsoft.quantum.overview.understanding) erklärt, stellt ein Qubit eine Einheit mit Quanteninformationen dar, die sich in einem Superpositionszustand befinden kann. Für ein Qubit kann sich bei einer Messung nur 0 oder 1 ergeben. Wenn jedoch ein Vorgang ausgeführt wird, stellt der Status des Qubit die Wahrscheinlichkeit dar, dass entweder 0 oder 1 mit einer Messung gelesen wird. Dieser Wahrscheinlichkeitszustand wird als Überlagerung bezeichnet. Wir können diese Wahrscheinlichkeit verwenden, um Zufallszahlen zu generieren.

In unserem Q# Vorgang stellen wir den `Qubit` DataType, den systemeigenen, bereit Q# . Wir können `Qubit` nur mit einer `using`-Anweisung zuordnen. Nach der Zuordnung befindet sich ein Qubit immer im Zustand `Zero`. 

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

Nachdem wir nun über einen-Vorgang verfügen, mit Q# dem zufällige Bits generiert werden, können wir damit einen kompletten Quantum-Zufallszahlengenerator erstellen. Wir können eine- Q# Anwendung verwenden oder ein Host Programm verwenden.



### <a name="no-locq-applications-with-visual-studio-or-visual-studio-code"></a>[Q# Anwendungen mit Visual Studio oder Visual Studio Code](#tab/tabid-qsharp)

Q#Fügen Sie dem Programm den folgenden Einstiegspunkt hinzu, um die vollständige Anwendung zu erstellen Q# : 

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="17-33":::

Abhängig von der Projekt Konfiguration und den Befehlszeilenoptionen führt das Programm den Vorgang oder die Funktion aus, der mit dem- `@EntryPoint()` Attribut für einen Simulator oder eine Ressourcenschätzung gekennzeichnet ist.

:::code language="qsharp" source="~/quantum/samples/getting-started/qrng/Qrng.qs" range="3-34":::

Drücken Sie in Visual Studio einfach STRG + F5, um das Skript auszuführen.

Erstellen Sie in VS Code erstmalig die Datei „Program.qs“, indem Sie Folgendes im Terminal eingeben:

```dotnetcli
dotnet build
```

Bei nachfolgenden Ausführungen muss diese Datei nicht erneut erstellt werden. Geben Sie für die Ausführung den folgenden Befehl ein, und drücken Sie die EINGABETASTE:

```dotnetcli
dotnet run --no-build
```

### <a name="python-with-visual-studio-code-or-the-command-prompt"></a>[Python mit Visual Studio Code oder der Eingabeaufforderung](#tab/tabid-python)

Um Ihr neues Q# Programm aus python auszuführen, speichern Sie den folgenden Code `host.py` :

:::code language="python" source="~/quantum/samples/interoperability/qrng/host.py" range="11-30":::

Anschließend können Sie Ihr python-Host Programm an der Eingabeaufforderung ausführen:

```bash
$ python host.py
Preparing Q# environment...
..The random number generated is 42
```

### <a name="c-with-visual-studio-code-or-visual-studio"></a>[C# mit Visual Studio Code oder Visual Studio](#tab/tabid-csharp)

Um Q# das neue Programm aus c# auszuführen, ändern `Driver.cs` Sie, um den folgenden c#-Code einzuschließen:

:::code language="csharp" source="~/quantum/samples/interoperability/qrng/Host.cs" range="4-39":::

Sie können dann Ihr c#-Host Programm von der Eingabeaufforderung aus ausführen (in Visual Studio sollten Sie F5 drücken):

```bash
$ dotnet run
The random number generated is 42
```

***
