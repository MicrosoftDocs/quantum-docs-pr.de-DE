---
uid: Microsoft.Quantum.Math.BitSizeI
title: Bitsizei-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: BitSizeI
qsharp.summary: >-
  For a non-negative integer `a`, returns the number of bits required to represent `a`.

  That is, returns the smallest $n$ such that $a < 2^n$.
ms.openlocfilehash: e7edf37a81571dfa1d4cb755493e1863a44c694e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857699"
---
# <a name="bitsizei-function"></a>Bitsizei-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt für eine nicht negative ganze `a` Zahl die Anzahl der Bits zurück, die zur Darstellung von erforderlich sind `a` .

Das heißt, die kleinste $n $ wird so zurückgegeben, dass $a < 2 ^ n $.

```qsharp
function BitSizeI (a : Int) : Int
```


## <a name="input"></a>Eingabe

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)

Die ganze Zahl, deren bitgröße berechnet werden soll.



## <a name="output--int"></a>Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)

Die bitgröße von `a` .