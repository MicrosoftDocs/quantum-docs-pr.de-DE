---
title: Erstellen eines Quanten-Zufallszahlengenerators
description: Enthält eine Beschreibung der Erstellung eines Q#-Projekts, mit dem grundlegende Quantenkonzepte wie die Überlagerung veranschaulicht werden, indem ein Quanten-Zufallszahlengenerator erstellt wird.
author: bromeg
ms.author: megbrow@microsoft.com
ms.date: 10/25/2019
ms.topic: article
uid: microsoft.quantum.quickstarts.qrng
ms.openlocfilehash: c3039b92c4b3235a397d5cf31280ac2673706e9d
ms.sourcegitcommit: 2ca4755d1a63431e3cb2d2918a10ad477ec2e368
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2019
ms.locfileid: "73462838"
---
# <a name="quickstart-implement-a-quantum-random-number-generator-in-q"></a>Schnellstart: Implementieren eines Quanten-Zufallszahlengenerators in Q#
Ein einfaches Beispiel für einen Quantenalgorithmus, der in Q# geschrieben ist, ist ein Quanten-Zufallszahlengenerator. Für diesen Algorithmus wird das Prinzip der Quantenmechanik genutzt, um eine Zufallszahl zu generieren. 

## <a name="prerequisites"></a>Voraussetzungen

- Das Microsoft [Quantum Development Kit](xref:microsoft.quantum.install).
- [Erstellen eines Q#-Projekts](xref:microsoft.quantum.howto.createproject)


## <a name="write-a-q-operation"></a>Schreiben einer Q#-Operation

### <a name="q-operation-code"></a>Q#-Operationscode

1. Ersetzen Sie den Inhalt der Datei „Operation.qs“ durch den folgenden Code:

    ```qsharp
    namespace Quantum {
        open Microsoft.Quantum.Intrinsic;

        operation QuantumRandomNumberGenerator() : Result {
            using(q = Qubit())  { // Allocate a qubit.
                H(q);             // Put the qubit to superposition. It now has a 50% chance of being 0 or 1.
                let r = M(q);     // Measure the qubit value.
                Reset(q);
                return r;
            }
        }
    }
    ```

Wie im Artikel [Was ist Quantencomputing?](xref:microsoft.quantum.overview.what) erwähnt, stellt ein Qubit eine Einheit mit Quanteninformationen dar, für die eine Überlagerung vorliegen kann. Für ein Qubit kann sich bei einer Messung nur 0 oder 1 ergeben. Während der Ausführung steht der Zustand des Qubits aber für die Wahrscheinlichkeit, dass sich für eine Messung entweder 0 oder 1 ergibt. Dieser Wahrscheinlichkeitszustand wird als Überlagerung bezeichnet. Wir können diese Wahrscheinlichkeit verwenden, um Zufallszahlen zu generieren.

In unserer Q#-Operation führen wir den nativen Q#-Datentyp `Qubit` ein. Wir können `Qubit` nur mit einer `using`-Anweisung zuordnen. Nach der Zuordnung befindet sich ein Qubit immer im Zustand `Zero`. 

Mit der Operation `H` können wir das `Qubit` in den Zustand der Überlagerung versetzen. Zum Messen eines Qubits und Lesen seines Werts verwenden Sie die intrinsische Operation `M`.

Indem wir das `Qubit` in den Zustand der Überlagerung versetzen und die Messung durchführen, ergibt sich bei jedem Codeaufruf ein anderer Wert als Ergebnis. 

Wenn die Zuordnung für ein `Qubit` aufgehoben wird, muss es explizit zurück in den Zustand `Zero` versetzt werden. Andernfalls wird vom Simulator ein Laufzeitfehler gemeldet. Eine einfache Möglichkeit, dies zu erreichen, ist das Aufrufen von `Reset`.

### <a name="visualizing-the-code-with-the-bloch-sphere"></a>Visualisieren des Codes mit der Bloch-Kugel

Bei der Bloch-Kugel steht der Nordpol für den klassischen Wert **0** und der Südpol für den klassischen Wert **1**. Jede Überlagerung kann durch einen Punkt auf der Kugel dargestellt werden (per Pfeil). Je näher sich das Ende des Pfeils an einem der Pole befindet, desto höher ist die Wahrscheinlichkeit, dass das Qubit bei einer Messung auf den klassischen Wert zurückfällt, der dem Pol zugeordnet ist. Der unten durch den roten Pfeil dargestellte Qubit-Zustand verfügt beispielsweise über eine höhere Wahrscheinlichkeit, dass sich bei einer Messung der Wert **0** ergibt.

<img src="./Bloch.svg" width="175">

Wir können diese Darstellung verwenden, um die Aktivitäten des Codes zu visualisieren:

* Wir beginnen mit einem im Zustand **0** initialisierten Qubit und wenden `H` an, um eine Überlagerung zu erstellen, bei der die Wahrscheinlichkeiten für **0** und **1** gleich hoch sind.

<img src="./H.svg" width="450">

* Anschließend messen wir das Qubit und speichern die Ausgabe:

<img src="./Measurement2.svg" width="450">

Da das Ergebnis der Messung völlig zufällig ist, erhalten wir ein zufälliges Bit. Wir können diesen Vorgang mehrmals aufrufen, um ganze Zahlen zu erstellen. Wenn wir den Vorgang beispielsweise dreimal aufrufen, um drei zufällige Bits zu erhalten, können wir zufällige 3-Bit-Zahlen erstellen (also eine Zufallszahl zwischen 0 und 7).
