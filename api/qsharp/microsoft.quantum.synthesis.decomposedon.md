---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: Debug-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: fb7aa5af8f3eb07399e0d2dd2d50723f4e6b169a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855529"
---
# <a name="decomposedon-function"></a>Debug-Funktion

Namespace: [Microsoft. Quantum. Synthese](xref:Microsoft.Quantum.Synthesis)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Zerlegt eine permutations für eine Variable.

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a>Beschreibung

Bei Angabe einer permutations $ \pi $ ( `perm` ) und eines Index $i $ ( `index` ), diese Methode gibt drei Permutationen $ ((\ pi_l, \ pi_r), \pi ') $ so zurück, dass die Bilder von $ \ pi_l $ und $ \ pi_r $ Bits in ihren Elementen bei anderen Indizes als $i $ und Bilder von $ \pi ' $ do not Change Bit $i $ in ihren Elementen nicht ändern.

## <a name="input"></a>Eingabe

### <a name="perm--int"></a>Perm: [int](xref:microsoft.quantum.lang-ref.int)[]




### <a name="index--int"></a>Index: [int](xref:microsoft.quantum.lang-ref.int)





## <a name="output--intintint"></a>Ausgabe: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])



## <a name="example"></a>Beispiel

Angenommen, die Eingabe ist "Perm = [0, 2, 3, 5, 7, 1, 4, 6]" und "Index = 0". dann berechnet diese Funktion drei Permutationen basierend auf der folgenden Tabelle, in der die permutations `perm` in Binär Notation mit Elementen in Gruppe A und Bilder in Gruppe D aufgelistet ist.  In den Spalten werden die bitindizes aufgelistet.

|   A |   B |   C |   D |
| 2 1 0 | 2 1 0 | 2 1 0 | 2 1 0 |
|-------|-------|-------|-------|
| 0 0 0 |       |       | 0 0 0 | 0
| 0 0 1 |       |       | 0 1 0 | 2
| 0 1 0 |       |       | 0 1 1 | 3
| 0 1 1 |       |       | 1 0 1 | 5
| 1 0 0 |       |       | 1 1 1 | 7
| 1 0 1 |       |       | 0 0 1 | 1
| 1 1 0 |       |       | 1 0 0 | 4
| 1 1 1 |       |       | 1 1 0 | 6

Alle Werte für Indizes ungleich 0 (= Index) werden von A nach B und von D in C kopiert.

|   A |   B |   C |   D |
| 2 1 0 | 2 1 0 | 2 1 0 | 2 1 0 |
|-------|-------|-------|-------|
| 0 0 0 | 0 0   | 0 0   | 0 0 0 |
| 0 0 1 | 0 0   | 0 1   | 0 1 0 |
| 0 1 0 | 0 1   | 0 1   | 0 1 1 |
| 0 1 1 | 0 1   | 1 0   | 1 0 1 |
| 1 0 0 | 1 0   | 1 1   | 1 1 1 |
| 1 0 1 | 1 0   | 0 0   | 0 0 1 |
| 1 1 0 | 1 1   | 1 0   | 1 0 0 |
| 1 1 1 | 1 1   | 1 1   | 1 1 0 |

Im nächsten Schritt wird ein Wert von 0 für das erste Element mit einem leeren Index in der Spalte 0 in Block B eingefügt. Anschließend wird 1 in B eingefügt, wobei das Präfix übereinstimmt (im ersten Fall die andere Zeile mit den Indizes 0 0).
Anschließend wird ein 1 in der gleichen Zeile in Block c und dann ein 0 für das entsprechende Präfix in Block c hinzugefügt.  Dieser Prozess wird wiederholt, bis alle Indizes in den Blöcken B und C in Spalte 0 platziert wurden.

|   A |   B |   C |   D |
| 2 1 0 | 2 1 0 | 2 1 0 | 2 1 0 |
|-------|-------|-------|-------|
| 0 0 0 | 0 0 0 | 0 0 0 | 0 0 0 |
| 0 0 1 | 0 0 1 | 0 1 1 | 0 1 0 |
| 0 1 0 | 0 1 0 | 0 1 0 | 0 1 1 |
| 0 1 1 | 0 1 1 | 1 0 1 | 1 0 1 |
| 1 0 0 | 1 0 0 | 1 1 0 | 1 1 1 |
| 1 0 1 | 1 0 1 | 0 0 1 | 0 0 1 |
| 1 1 0 | 1 1 0 | 1 0 0 | 1 0 0 |
| 1 1 1 | 1 1 1 | 1 1 1 | 1 1 0 |

Wir können drei neue Permutationen aus der Tabelle lesen:

- $ \ pi_l $ mit Elementen in a, Bilder in B (links)
- $ \ pi_r $ mit Elementen in D, Bilder in C (right)
- $ \pi ' $ with Elements in B, Bilder in C (Rest)

Beachten Sie, dass die Bitwerte in $ \ pi_l $ und $ \ pi_r $ für die Indizes 1 und 2 nicht geändert werden, und die Bitwerte für in $ \ pi_ ' $ für Index 0 nicht geändert werden.  Beachten Sie außerdem, dass $ \ pi_l $ und $ \ pi_r $ selbst inversen müssen.

Die abgeleiteten und zurückgegebenen Permutationen lauten: Left = [0, 1, 2, 3, 4, 5, 6, 7] right = [0, 1, 3, 2, 4, 5, 7, 6] Restwert = [0, 3, 2, 5, 6, 1, 4, 7]