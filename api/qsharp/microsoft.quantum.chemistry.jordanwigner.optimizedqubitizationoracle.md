---
uid: Microsoft.Quantum.Chemistry.JordanWigner.OptimizedQubitizationOracle
title: Optimizedqubitizationoracle-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: OptimizedQubitizationOracle
qsharp.summary: Returns T-count optimized Qubitization operation and the parameters necessary to run it.
ms.openlocfilehash: da569e8ddad575b1ba1bbc2081a6a948cb675d48
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98837042"
---
# <a name="optimizedqubitizationoracle-function"></a><span data-ttu-id="fbb7a-102">Optimizedqubitizationoracle-Funktion</span><span class="sxs-lookup"><span data-stu-id="fbb7a-102">OptimizedQubitizationOracle function</span></span>

<span data-ttu-id="fbb7a-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="fbb7a-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="fbb7a-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="fbb7a-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="fbb7a-105">Gibt einen optimierten qubisierungsvorgang mit T-Anzahl und die für die Ausführung erforderlichen Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="fbb7a-105">Returns T-count optimized Qubitization operation and the parameters necessary to run it.</span></span>

```qsharp
function OptimizedQubitizationOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData, targetError : Double) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a><span data-ttu-id="fbb7a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fbb7a-106">Input</span></span>

### <a name="qsharpdata--jordanwignerencodingdata"></a><span data-ttu-id="fbb7a-107">qsharpdata: [jordanwignerencodingdata](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="fbb7a-107">qSharpData : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="fbb7a-108">Hamiltona wird nach `JordanWignerEncodingData` Format beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fbb7a-108">Hamiltonian described by `JordanWignerEncodingData` format.</span></span>


### <a name="targeterror--double"></a><span data-ttu-id="fbb7a-109">targeterror: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fbb7a-109">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fbb7a-110">Fehler bei der schrittweisen Vorbereitung des Zustands.</span><span class="sxs-lookup"><span data-stu-id="fbb7a-110">Error of auxillary state preparation step.</span></span>



## <a name="output--intdoublequbit--unit--is-adj--ctl"></a><span data-ttu-id="fbb7a-111">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL))</span><span class="sxs-lookup"><span data-stu-id="fbb7a-111">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl))</span></span>

<span data-ttu-id="fbb7a-112">Ein Tupel, in dem: `Int` die Anzahl der zugeordneten Qubits ist, `Double` die One-Norm von hamiltona-Koeffizienten ist, und der Vorgang ist der durch die qubisierung erstellte Quantum Walk.</span><span class="sxs-lookup"><span data-stu-id="fbb7a-112">A tuple where: `Int` is the number of qubits allocated, `Double` is the one-norm of Hamiltonian coefficients, and the operation is the Quantum walk created by Qubitization.</span></span>