---
uid: Microsoft.Quantum.ErrorCorrection.EncodeIntoSteaneCode
title: Encodeindesteanecode-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: EncodeIntoSteaneCode
qsharp.summary: An encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.
ms.openlocfilehash: e74c7fdc5acbb1a8c417bad3eb3630314e3f71bc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96201018"
---
# <a name="encodeintosteanecode-operation"></a><span data-ttu-id="b90fc-102">Encodeindesteanecode-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b90fc-102">EncodeIntoSteaneCode operation</span></span>

<span data-ttu-id="b90fc-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="b90fc-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="b90fc-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b90fc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b90fc-105">Ein Codierungs Vorgang, der ein uncodiertes Quantum-Register einem codierten Quantum-Register unter dem Quantum-Code ⟦ 7, 1, 3 ⟧ Steane zuordnet.</span><span class="sxs-lookup"><span data-stu-id="b90fc-105">An encoding operation that maps an unencoded quantum register to an encoded quantum register under the ⟦7, 1, 3⟧ Steane quantum code.</span></span>

```qsharp
operation EncodeIntoSteaneCode (physRegister : Qubit[], auxQubits : Qubit[]) : Microsoft.Quantum.ErrorCorrection.LogicalRegister
```


## <a name="input"></a><span data-ttu-id="b90fc-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b90fc-106">Input</span></span>

### <a name="physregister--qubit"></a><span data-ttu-id="b90fc-107">physregister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b90fc-107">physRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b90fc-108">Ein Qubit-Register, das den unverschlüsselten Quantenzustand enthält.</span><span class="sxs-lookup"><span data-stu-id="b90fc-108">A qubit register which holds the an unencoded quantum state</span></span>


### <a name="auxqubits--qubit"></a><span data-ttu-id="b90fc-109">"auxqubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]"</span><span class="sxs-lookup"><span data-stu-id="b90fc-109">auxQubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b90fc-110">Ein Qubit-Register, das anfänglich 0 (null) ist und dem Quantum-System hinzugefügt wird, sodass ein Codierungs Vorgang ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b90fc-110">A qubit register which is initially zero and which gets added to the quantum system so that an encoding operation can be performed</span></span>



## <a name="output--logicalregister"></a><span data-ttu-id="b90fc-111">Ausgabe: [logicalregister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span><span class="sxs-lookup"><span data-stu-id="b90fc-111">Output : [LogicalRegister](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)</span></span>

<span data-ttu-id="b90fc-112">Ein Quantum-Register mit dem Zustand, nachdem der Steane-Encoder angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b90fc-112">A quantum register holding the state after the Steane encoder has been applied</span></span>

## <a name="see-also"></a><span data-ttu-id="b90fc-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b90fc-113">See Also</span></span>

- [<span data-ttu-id="b90fc-114">Microsoft. Quantum. errorcorrection. logicalregister</span><span class="sxs-lookup"><span data-stu-id="b90fc-114">Microsoft.Quantum.ErrorCorrection.LogicalRegister</span></span>](xref:Microsoft.Quantum.ErrorCorrection.LogicalRegister)
- [<span data-ttu-id="b90fc-115">Microsoft. Quantum. errorcorrection. steanecodecodecoder</span><span class="sxs-lookup"><span data-stu-id="b90fc-115">Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder</span></span>](xref:Microsoft.Quantum.ErrorCorrection.SteaneCodeDecoder)