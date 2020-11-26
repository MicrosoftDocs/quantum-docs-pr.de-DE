---
uid: Microsoft.Quantum.Canon.GrayCode
title: Graycode-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: b15586c57180b00064721afc990436320824cba2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206883"
---
# <a name="graycode-function"></a>Graycode-Funktion

Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Erstellt graue Codesequenzen.

```qsharp
function GrayCode (n : Int) : (Int, Int)[]
```


## <a name="input"></a>Eingabe

### <a name="n--int"></a>n: [int](xref:microsoft.quantum.lang-ref.int)

Anzahl von Bits



## <a name="output--intint"></a>Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []

Array von Tupeln. Der erste Wert im Tupel ist der Wert in grau Punkt Sequenz zweiter Wert in Tupel ist Position, um den aktuellen Wert zu ändern, um den nächsten Wert zu erhalten.