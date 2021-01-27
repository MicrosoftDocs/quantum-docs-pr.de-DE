---
uid: Microsoft.Quantum.Canon.GrayCode
title: Graycode-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: GrayCode
qsharp.summary: Creates Gray code sequences
ms.openlocfilehash: 0a9a19685f0511c44942df7d0bc8d257ad6b18c6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840497"
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

## <a name="example"></a>Beispiel

```qsharp
GrayCode(2); // [(0, 0),(1, 1),(3, 0),(2, 1)]
```