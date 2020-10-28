---
uid: Microsoft.Quantum.Canon.GrayCode
title: Graycode-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: fc673ae21a952788b5beb74c1bad94ee9fe54480
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704167"
---
# <a name="graycode-function"></a>Graycode-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paketen [](https://nuget.org/packages/)


Erstellt graue Codesequenzen.

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a>Eingabe

### <a name="n--int"></a>n: [int](xref:microsoft.quantum.lang-ref.int)

Anzahl von Bits



## <a name="output--intint"></a>Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []

Array von Tupeln. Der erste Wert im Tupel ist der Wert in grau Punkt Sequenz zweiter Wert in Tupel ist Position, um den aktuellen Wert zu ändern, um den nächsten Wert zu erhalten.