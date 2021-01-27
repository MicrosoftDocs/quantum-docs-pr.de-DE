---
uid: Microsoft.Quantum.Chemistry.JordanWigner._JordanWignerOptimizedBlockEncodingQubitManager_
title: _Jordanwigneroptimizedblockencodingqubitmanager_ -Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _JordanWignerOptimizedBlockEncodingQubitManager_
qsharp.summary: ''
ms.openlocfilehash: ac7785142879a19d67caaf3fcbde5dc95e566c1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851595"
---
# <a name="_jordanwigneroptimizedblockencodingqubitmanager_-function"></a><span data-ttu-id="9a6d0-102">_Jordanwigneroptimizedblockencodingqubitmanager_ -Funktion</span><span class="sxs-lookup"><span data-stu-id="9a6d0-102">_JordanWignerOptimizedBlockEncodingQubitManager_ function</span></span>

<span data-ttu-id="9a6d0-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="9a6d0-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="9a6d0-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="9a6d0-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>




```qsharp
function _JordanWignerOptimizedBlockEncodingQubitManager_ (targetError : Double, nCoeffs : Int, nZ : Int, nMaj : Int, nIdxRegQubits : Int, ctrlRegister : Qubit[]) : ((Microsoft.Quantum.Arithmetic.LittleEndian, Qubit[], Qubit, Qubit[], Qubit[], Qubit[], Microsoft.Quantum.Arithmetic.LittleEndian, Microsoft.Quantum.Arithmetic.LittleEndian[]), (Qubit, Qubit[], Qubit[], Qubit[], Microsoft.Quantum.Arithmetic.LittleEndian[]), Qubit[])
```


## <a name="input"></a><span data-ttu-id="9a6d0-105">Eingabe</span><span class="sxs-lookup"><span data-stu-id="9a6d0-105">Input</span></span>

### <a name="targeterror--double"></a><span data-ttu-id="9a6d0-106">targeterror: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9a6d0-106">targetError : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="ncoeffs--int"></a><span data-ttu-id="9a6d0-107">ncoeffs: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9a6d0-107">nCoeffs : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="nz--int"></a><span data-ttu-id="9a6d0-108">NZ: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9a6d0-108">nZ : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="nmaj--int"></a><span data-ttu-id="9a6d0-109">nmaj: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9a6d0-109">nMaj : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="nidxregqubits--int"></a><span data-ttu-id="9a6d0-110">nidxregqubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9a6d0-110">nIdxRegQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="ctrlregister--qubit"></a><span data-ttu-id="9a6d0-111">ctrlregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9a6d0-111">ctrlRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>





## <a name="output--littleendianqubitqubitqubitqubitqubitlittleendianlittleendianqubitqubitqubitqubitlittleendianqubit"></a><span data-ttu-id="9a6d0-112">Output: (([littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)[]), ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[littleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)[]),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span><span class="sxs-lookup"><span data-stu-id="9a6d0-112">Output : (([LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian),[LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)[]),([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)[]),[Qubit](xref:microsoft.quantum.lang-ref.qubit)[])</span></span>

