---
uid: Microsoft.Quantum.Chemistry.JordanWigner.QubitizationOracle
title: Qubitizationoracle-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: QubitizationOracle
qsharp.summary: Returns Qubitization operation and the parameters necessary to run it.
ms.openlocfilehash: cf6fe04b3f629c4ca4a7c27d8519a4cb42d07630
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98835832"
---
# <a name="qubitizationoracle-function"></a><span data-ttu-id="f7f1c-102">Qubitizationoracle-Funktion</span><span class="sxs-lookup"><span data-stu-id="f7f1c-102">QubitizationOracle function</span></span>

<span data-ttu-id="f7f1c-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="f7f1c-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="f7f1c-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f7f1c-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="f7f1c-105">Gibt den qubisierungsvorgang und die für die Ausführung erforderlichen Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-105">Returns Qubitization operation and the parameters necessary to run it.</span></span>

```qsharp
function QubitizationOracle (qSharpData : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData) : (Int, (Double, (Qubit[] => Unit is Adj + Ctl)))
```


## <a name="input"></a><span data-ttu-id="f7f1c-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f7f1c-106">Input</span></span>

### <a name="qsharpdata--jordanwignerencodingdata"></a><span data-ttu-id="f7f1c-107">qsharpdata: [jordanwignerencodingdata](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span><span class="sxs-lookup"><span data-stu-id="f7f1c-107">qSharpData : [JordanWignerEncodingData](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerEncodingData)</span></span>

<span data-ttu-id="f7f1c-108">Hamiltona wird nach `JordanWignerEncodingData` Format beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-108">Hamiltonian described by `JordanWignerEncodingData` format.</span></span>



## <a name="output--intdoublequbit--unit--is-adj--ctl"></a><span data-ttu-id="f7f1c-109">Ausgabe: ([int](xref:microsoft.quantum.lang-ref.int), ([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist ADJ + CTL))</span><span class="sxs-lookup"><span data-stu-id="f7f1c-109">Output : ([Int](xref:microsoft.quantum.lang-ref.int),([Double](xref:microsoft.quantum.lang-ref.double),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl))</span></span>

<span data-ttu-id="f7f1c-110">Ein Tupel, in dem: `Int` die Anzahl der zugeordneten Qubits ist, `Double` die One-Norm von hamiltona-Koeffizienten ist, und der Vorgang ist der durch die qubisierung erstellte Quantum Walk.</span><span class="sxs-lookup"><span data-stu-id="f7f1c-110">A tuple where: `Int` is the number of qubits allocated, `Double` is the one-norm of Hamiltonian coefficients, and the operation is the Quantum walk created by Qubitization.</span></span>