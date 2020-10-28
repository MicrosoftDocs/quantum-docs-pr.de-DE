---
uid: Microsoft.Quantum.Canon.MultiplexerFromGenerator
title: Multiplexerfromgenerator-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexerFromGenerator
qsharp.summary: >-
  Returns a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: 327d995d3870732887f880778eb289c3aad1f030
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704010"
---
# <a name="multiplexerfromgenerator-function"></a><span data-ttu-id="da0a0-102">Multiplexerfromgenerator-Funktion</span><span class="sxs-lookup"><span data-stu-id="da0a0-102">MultiplexerFromGenerator function</span></span>

<span data-ttu-id="da0a0-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="da0a0-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="da0a0-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="da0a0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="da0a0-105">Gibt einen mehrfach kontrollierten einheitlichen Vorgang $U $ zurück, der eine einheitliche $V _J $ anwendet, wenn dies durch den n-Qubit-Zahlen Status $ \ket{j} $ gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="da0a0-105">Returns a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="da0a0-106">$U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.</span><span class="sxs-lookup"><span data-stu-id="da0a0-106">$U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
function MultiplexerFromGenerator (unitaryGenerator : (Int, (Int -> (Qubit[] => Unit is Adj + Ctl)))) : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="da0a0-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="da0a0-107">Input</span></span>

### <a name="unitarygenerator--intint---qubit--unit-adj--ctl"></a><span data-ttu-id="da0a0-108">unitarygenerator: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL)</span><span class="sxs-lookup"><span data-stu-id="da0a0-108">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl)</span></span>

<span data-ttu-id="da0a0-109">Ein Tupel, bei dem das erste Element `Int` die Anzahl von uniflüssen $N $ und das zweite Element `(Int -> ('T => () is Adj + Ctl))` eine Funktion ist, die eine ganze Zahl $j $ in $ [0, N-1] $ annimmt und den einheitlichen Vorgang $V _J $ ausgibt.</span><span class="sxs-lookup"><span data-stu-id="da0a0-109">A tuple where the first element `Int` is the number of unitaries $N$, and the second element `(Int -> ('T => () is Adj + Ctl))` is a function that takes an integer $j$ in $[0,N-1]$ and outputs the unitary operation $V_j$.</span></span>



## <a name="output--littleendianqubit--unit-adj--ctl"></a><span data-ttu-id="da0a0-110">Ausgabe: ([littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="da0a0-110">Output : ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="da0a0-111">Ein mehrfach kontrollierter einheitlicher Vorgang $U $, der die von beschriebenen uniervorgänge anwendet `unitaryGenerator` .</span><span class="sxs-lookup"><span data-stu-id="da0a0-111">A multiply-controlled unitary operation $U$ that applies unitaries described by `unitaryGenerator`.</span></span>

## <a name="see-also"></a><span data-ttu-id="da0a0-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="da0a0-112">See Also</span></span>

- [<span data-ttu-id="da0a0-113">Microsoft. Quantum. Canon. multiplexoperationsfromgenerator</span><span class="sxs-lookup"><span data-stu-id="da0a0-113">Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator</span></span>](xref:Microsoft.Quantum.Canon.MultiplexOperationsFromGenerator)