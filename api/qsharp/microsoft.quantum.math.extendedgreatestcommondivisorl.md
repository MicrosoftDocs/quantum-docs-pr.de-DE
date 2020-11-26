---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorL
title: Extendedgreatestcommondivisorl-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorL
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: abbbd367859952180f181a245ca0754646529b18
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210708"
---
# <a name="extendedgreatestcommondivisorl-function"></a>Extendedgreatestcommondivisorl-Funktion

Namespace: [Microsoft. Quantum. Math](xref:Microsoft.Quantum.Math)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Berechnet ein Tupel $ (u, v) $, sodass $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $, wobei $ \operatschmue{GCD} $ $a $ Greatest common divisor von $a $ und $b $ ist. Die GCD ist immer positiv.

```qsharp
function ExtendedGreatestCommonDivisorL (a : BigInt, b : BigInt) : (BigInt, BigInt)
```


## <a name="input"></a>Eingabe

### <a name="a--bigint"></a>a: [bigint](xref:microsoft.quantum.lang-ref.bigint)

die erste Zahl, die der erweiterte größte gemeinsame Divisor berechnet wird.


### <a name="b--bigint"></a>b: [bigint](xref:microsoft.quantum.lang-ref.bigint)

die zweite Zahl, von der der erweiterte größte gemeinsame Divisor berechnet wird.



## <a name="output--bigintbigint"></a>Ausgabe: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))

Tuple $ (u, v) $ mit der-Eigenschaft $u \cdot a + v \cdot b = \operatschmue{GCD} (a, b) $.

## <a name="references"></a>Referenzen

- Diese Implementierung ist gemäß https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm