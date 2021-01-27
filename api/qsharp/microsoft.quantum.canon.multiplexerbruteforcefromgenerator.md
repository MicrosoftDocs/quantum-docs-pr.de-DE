---
uid: Microsoft.Quantum.Canon.MultiplexerBruteForceFromGenerator
title: Multiplexerbruteforcefromgenerator-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexerBruteForceFromGenerator
qsharp.summary: >-
  Returns a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.

  $U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.
ms.openlocfilehash: d3606ff4f45765fd3aaf1e6a3078288b214349d0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852565"
---
# <a name="multiplexerbruteforcefromgenerator-function"></a><span data-ttu-id="a1a39-102">Multiplexerbruteforcefromgenerator-Funktion</span><span class="sxs-lookup"><span data-stu-id="a1a39-102">MultiplexerBruteForceFromGenerator function</span></span>

<span data-ttu-id="a1a39-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a1a39-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a1a39-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a1a39-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a1a39-105">Gibt einen mehrfach kontrollierten einheitlichen Vorgang $U $ zurück, der eine einheitliche $V _J $ anwendet, wenn dies durch den n-Qubit-Zahlen Status $ \ket{j} $ gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="a1a39-105">Returns a multiply-controlled unitary operation $U$ that applies a unitary $V_j$ when controlled by n-qubit number state $\ket{j}$.</span></span>

<span data-ttu-id="a1a39-106">$U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j}\otimes V_j $.</span><span class="sxs-lookup"><span data-stu-id="a1a39-106">$U = \sum^{2^n-1}_{j=0}\ket{j}\bra{j}\otimes V_j$.</span></span>

```qsharp
function MultiplexerBruteForceFromGenerator (unitaryGenerator : (Int, (Int -> (Qubit[] => Unit is Adj + Ctl)))) : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="a1a39-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="a1a39-107">Input</span></span>

### <a name="unitarygenerator--intint---qubit--unit--is-adj--ctl"></a><span data-ttu-id="a1a39-108">unitarygenerator: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL)</span><span class="sxs-lookup"><span data-stu-id="a1a39-108">unitaryGenerator : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int) -> [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl)</span></span>

<span data-ttu-id="a1a39-109">Ein Tupel, bei dem das erste Element `Int` die Anzahl von uniflüssen $N $ und das zweite Element `(Int -> ('T => () is Adj + Ctl))` eine Funktion ist, die eine ganze Zahl $j $ in $ [0, N-1] $ annimmt und den einheitlichen Vorgang $V _J $ ausgibt.</span><span class="sxs-lookup"><span data-stu-id="a1a39-109">A tuple where the first element `Int` is the number of unitaries $N$, and the second element `(Int -> ('T => () is Adj + Ctl))` is a function that takes an integer $j$ in $[0,N-1]$ and outputs the unitary operation $V_j$.</span></span>



## <a name="output--littleendianqubit--unit--is-adj--ctl"></a><span data-ttu-id="a1a39-110">Ausgabe: ([littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="a1a39-110">Output : ([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a1a39-111">Ein mehrfach kontrollierter einheitlicher Vorgang $U $, der die von beschriebenen uniervorgänge anwendet `unitaryGenerator` .</span><span class="sxs-lookup"><span data-stu-id="a1a39-111">A multiply-controlled unitary operation $U$ that applies unitaries described by `unitaryGenerator`.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1a39-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a1a39-112">See Also</span></span>

- [<span data-ttu-id="a1a39-113">Microsoft. Quantum. Canon. multiplexerbruteforcefromgenerator</span><span class="sxs-lookup"><span data-stu-id="a1a39-113">Microsoft.Quantum.Canon.MultiplexerBruteForceFromGenerator</span></span>](xref:Microsoft.Quantum.Canon.MultiplexerBruteForceFromGenerator)