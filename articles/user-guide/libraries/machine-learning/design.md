---
title: Entwerfen Sie Ihren eigenen Klassifizierer mit dem QDK
description: Lernen Sie die grundlegenden Konzepte für das Entwerfen von Verbindungs Modellen für den Quantum Circuit zentrierten Klassifizierer kennen.
author: geduardo
ms.author: v-edsanc@microsoft.com
ms.date: 02/17/2020
ms.topic: article
uid: microsoft.quantum.libraries.machine-learning.design
ms.openlocfilehash: b304b9d1a15f164f4dfe758aaed31b7b2369b18c
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275150"
---
# <a name="design-your-own-classifier"></a>Entwerfen Ihres eigenen Klassifizierers

In diesem Handbuch lernen Sie die grundlegenden Konzepte kennen, die hinter dem Entwurf von Leitungs Modellen für den Quantum Circuit zentrischen Klassifizierer stehen.

Wie bei klassischem Deep Learning gibt es keine allgemeine Regel für die Auswahl einer bestimmten Architektur. Abhängig vom Problem werden einige Architekturen besser als andere funktionieren. Es gibt jedoch einige Konzepte, die beim Entwerfen der Verbindung hilfreich sein könnten:

- Eine große Anzahl von Parametern impliziert ein flexibleres Modell, das möglicherweise zum Zeichnen komplexer Klassifizierungs Grenzen geeignet ist, aber auch anfälliger für die über Anpassung ist.

- Das Entwirren von Gates zwischen Qubits ist für die Erfassung der Korrelationen zwischen den Quantum-Features von entscheidender Bedeutung.

## <a name="how-to-build-a-classifier-with-q"></a>Erstellen eines Klassifizierers mit Q\#

Zum Erstellen einer Klassifizierer werden parametegesteuerte Rotationen in unserem Verbindungs Modell verkettet. Hierfür können wir den [`ControlledRotation`](xref:microsoft.quantum.machinelearning.controlledrotation) in der Quantum-Machine Learning Bibliothek definierten Typ verwenden. Dieser Typ akzeptiert vier Argumente, die bestimmen: den Index des Ziel-Qubit, das Array von Indizes der Steuerelement-Qubits, die Achse der Drehung und den Index des zugeordneten Parameters im Array von Parametern, die das Modell definieren.

Sehen wir uns ein Beispiel für einen Klassifizierer an. Im [Halbmond Beispiel](https://github.com/microsoft/Quantum/tree/master/samples/machine-learning/half-moons)finden Sie den folgenden Klassifizierer, der in der Datei definiert ist `Training.qs` .

```qsharp
    function ClassifierStructure() : ControlledRotation[] {
        return [
            ControlledRotation((0, new Int[0]), PauliX, 4),
            ControlledRotation((0, new Int[0]), PauliZ, 5),
            ControlledRotation((1, new Int[0]), PauliX, 6),
            ControlledRotation((1, new Int[0]), PauliZ, 7),
            ControlledRotation((0, [1]), PauliX, 0),
            ControlledRotation((1, [0]), PauliX, 1),
            ControlledRotation((1, new Int[0]), PauliZ, 2),
            ControlledRotation((1, new Int[0]), PauliX, 3)
        ];
    }
 ```

Hier definieren wir eine Funktion, die ein Array von Elementen zurückgibt `ControlledRotation` , das mit einem Array von Parametern verknüpft ist, und ein Bias definiert das [`SequentialModel`](xref:microsoft.quantum.machinelearning.sequentialmodel) . Dieser Typ ist in der Quantum-Machine Learning Bibliothek von grundlegender Bedeutung und definiert den Klassifizierer. Die in der obigen Funktion definierte Verbindung ist Teil eines Klassifizierers, in dem jede Stichprobe des Datasets zwei Funktionen enthält. Daher benötigen wir nur zwei Qubits. Die grafische Darstellung der Verbindung lautet wie folgt:

 ![Beispiel für Verbindungs Modell](~/media/circuit_model_1.PNG)

## <a name="use-the-library-functions-to-write-layers-of-gates"></a>Verwenden der Bibliotheksfunktionen zum Schreiben von Ebenen von Gates

Angenommen, wir verfügen über ein DataSet mit 784-Features pro Instanz, z. b. Bilder mit 28 × 28 Pixeln wie dem mnist-DataSet. In diesem Fall wird die Breite der Verbindung so groß, dass das manuelle Schreiben jedes einzelnen Gates zu einer möglichen, aber unpraktischen Aufgabe wird. Aus diesem Grund stellt die Quantum-Machine Learning Bibliothek eine Reihe von Tools zum automatischen Generieren von Ebenen von parametersierten Rotationen bereit. Die-Funktion gibt beispielsweise [`LocalRotationsLayer`](xref:microsoft.quantum.machinelearning.localrotationslayer) ein Array von unkontrollierten Single-Qubit-Drehungen an einer gegebenen Achse zurück, wobei für jedes Qubit im Register jeweils eine Drehung durch einen anderen Modellparameter angegeben wird. Gibt beispielsweise `LocalRotationsLayer(4, X)` den folgenden Satz von Gates zurück:

 ![Lokale rotationsebene](~/media/local_rotations_layer.PNG)

Wir empfehlen Ihnen, die [API-Referenz der Quantum Machine Learning Library](xref:microsoft.quantum.machinelearning) zu erkunden, um alle verfügbaren Tools zum Optimieren des Leitungs Entwurfs zu ermitteln.

## <a name="next-steps"></a>Nächste Schritte

 Testen Sie verschiedene Strukturen in den Beispielen, die von den Beispielen bereitgestellt werden. Werden Änderungen an der Leistung des Modells angezeigt? Im nächsten Tutorial, [`Load your own datasets`](xref:microsoft.quantum.libraries.machine-learning.load) , erfahren Sie, wie Datasets geladen werden, um neue Architektur von Klassifizierern zu testen.
