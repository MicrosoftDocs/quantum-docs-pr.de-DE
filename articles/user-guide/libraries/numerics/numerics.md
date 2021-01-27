---
title: Verwenden der Microsoft Q# Numerics-Bibliothek
description: Erfahren Sie mehr über die Typen und Vorgänge, die in der Microsoft Quantum-Numerics-Bibliothek verfügbar sind.
author: thomashaener
ms.author: thhaner
ms.date: 5/14/2019
ms.topic: conceptual
uid: microsoft.quantum.numerics.usage
no-loc:
- Q#
- $$v
ms.openlocfilehash: 92efd3b8677d2f27bc59f986ce6c9e915cd23652
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856440"
---
# <a name="using-the-numerics-library"></a>Verwenden der Numerics-Bibliothek

## <a name="overview"></a>Übersicht

Die Numerics-Bibliothek besteht aus drei Komponenten.

1. **Einfache ganzzahlige Arithmetik** mit ganzzahligen addern und Comparatoren
1. Allgemeine **ganzzahlige Funktionalität** , die auf Grundlage der grundlegenden Funktionalität basiert. Es umfasst Multiplikation, Division, Inversion usw.  für ganze Zahlen mit und ohne Vorzeichen.
1. **Arithmetische Funktionalität mit festem Punkt** mit Initialisierung mit festem Punkt, Addition, Multiplikation, gegenseitiger Auswertung, polynomgebung und Messung.

Auf alle diese Komponenten kann mit einer einzelnen-Anweisung zugegriffen werden `open` :
```qsharp
open Microsoft.Quantum.Arithmetic;
```

## <a name="types"></a>Typen

Die Numerics-Bibliothek unterstützt die folgenden Typen:

1. **`LittleEndian`**: Ein Qubit-Array `qArr : Qubit[]` , das eine Ganzzahl darstellt, wobei `qArr[0]` das unwichtigste Bit bezeichnet.
1. **`SignedLittleEndian`**: Identisch `LittleEndian` mit, mit der Ausnahme, dass es sich um eine ganze Zahl mit Vorzeichen handelt, die in zwei-
1. **`FixedPoint`**: Stellt eine reelle Zahl dar, die aus einem Qubit `qArr2 : Qubit[]` -Array und einer binären Punktposition besteht `pos` , die die Anzahl der binären Ziffern links vom binären Punkt zählt. `qArr2` wird auf die gleiche Weise wie gespeichert `SignedLittleEndian` .

## <a name="operations"></a>Operationen (Operations)

Für jeden der drei oben genannten Typen stehen eine Vielzahl von Vorgängen zur Verfügung:

1. **`LittleEndian`**
    - Addition
    - Vergleich
    - Multiplikation
    - Quadrieren
    - Division (mit Rest)

1. **`SignedLittleEndian`**
    - Addition
    - Vergleich
    - Inversion von Modulo 2
    - Multiplikation
    - Quadrieren

1. **`FixedPoint`**
    - Vorbereitung/Initialisierung für klassische Werte
    - Addition (klassische Konstante oder andere Quantum-Fixpunkte)
    - Vergleich
    - Multiplikation
    - Quadrieren
    - Polynomial Evaluation with Spezialisierung for even and Odd Functions
    - Gegenseitige (1/x)
    - Messung (klassisches Double)

Weitere Informationen und eine ausführliche Dokumentation zu den einzelnen Vorgängen finden Sie in der Referenz Dokumentation der Q# Bibliothek unter [docs.Microsoft.com](https://docs.microsoft.com/quantum) .

## <a name="sample-integer-addition"></a>Beispiel: Hinzufügen einer Ganzzahl

Als einfaches Beispiel angenommen, der Vorgang ist $ $ \ket x\ket y\mapsto \ket x\ket {x + y} $ $, d. h. ein Vorgang, der eine n-Qubit-Ganzzahl $x $ und ein n-oder (n + 1)-Qubit-Register $y $ als Eingabe annimmt. letztere wird der Summe $ (x + y) Beachten Sie, dass die Summe berechnet wird, Modulo $2 ^ n $, wenn $y $ in einem $n $-Bit-Register gespeichert wird.

Mit dem Quantum Development Kit kann dieser Vorgang wie folgt angewendet werden:
```qsharp
operation TestMyAddition(xValue : Int, yValue : Int, n : Int) : Unit {
    using ((xQubits, yQubits) = (Qubit[n], Qubit[n]))
    {
        let x = LittleEndian(xQubits); // define bit order
        let y = LittleEndian(yQubits);
        
        ApplyXorInPlace(xValue, x); // initialize values
        ApplyXorInPlace(yValue, y);
        
        AddI(x, y); // perform addition x+y into y
        
        // ... (use the result)
    }
}
```

## <a name="sample-evaluating-smooth-functions"></a>Beispiel: Auswerten von Smooth Functions

Zum Auswerten von Smooth-Funktionen wie z. b. $ \sin (x) $ auf einem Quantum-Computer, bei dem $x $ eine Quantum- `FixedPoint` Zahl ist, stellt die-Numerics-Bibliothek des Quantum Development Kits die Vorgänge `EvaluatePolynomialFxP` und bereit `Evaluate[Even/Odd]PolynomialFxP` .

Mit dem ersten, `EvaluatePolynomialFxP` , kann ein Polynoms der Form $ $ P (x) = a_0 + a_1x + a_2x ^ 2 + \cdots + a_dx ^ d, $ $ ausgewertet werden, wobei $d $ den *Grad* angibt. Dazu benötigen Sie lediglich die Polynomen `[a_0,..., a_d]` (vom Typ `Double[]` ), die Eingabe `x : FixedPoint` und die Ausgabe `y : FixedPoint` (anfänglich NULL):
```qsharp
EvaluatePolynomialFxP([1.0, 2.0], x, y);
```
Das Ergebnis, $P (x) = 1 + 2x $, wird in gespeichert `yFxP` .

Die zweite, `EvaluateEvenPolynomialFxP` und der dritte, `EvaluateOddPolynomialFxP` , sind Spezialisierungs Fälle für die Fälle der geraden bzw. ungeraden Funktionen. Das heißt, bei einer geraden/ungeraden Funktion $f (x) $ und $ $ P_ {even} (x) = a_0 + A_1 x ^ 2 + a_2 x ^ 4 + \cdots + a_d x ^ {2D}, $ $ $f (x) $ ist für $P _ {even} (x) $ oder $P _ {Odd} (x): = x\cdot P_ {even} (x) $ gleich gut.
In Q# können diese beiden Fälle wie folgt behandelt werden:
```qsharp
EvaluateEvenPolynomialFxP([1.0, 2.0], x, y);
```
wertet $P _ {even} (x) = 1 + 2x ^ 2 $ aus, und
```qsharp
EvaluateOddPolynomialFxP([1.0, 2.0], x, y);
```
, der $P _ {Odd} (x) = x + 2X ^ 3 $ auswertet.

## <a name="more-samples"></a>Weitere Beispiele

Weitere Beispiele finden Sie im [hauptbeispielrepository](https://github.com/Microsoft/Quantum).

Klonen Sie zunächst das Repository, und öffnen Sie den `Numerics` Unterordner:

```bash
git clone https://github.com/Microsoft/Quantum.git
cd Quantum/samples/numerics
```

`cd`In einem der Beispiel Ordner, und führen Sie das Beispiel über aus.

```bash
dotnet run
```
