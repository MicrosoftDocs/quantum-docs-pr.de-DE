---
uid: Microsoft.Quantum.ErrorCorrection.SteaneCodeEncoderImpl
title: Steanecodeencoderimpl-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: SteaneCodeEncoderImpl
qsharp.summary: Private operation used to implement both the Steane code encoder and decoder.
ms.openlocfilehash: b843422a6007d01de9b57ec659c229b8ab0ad2e6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702419"
---
# <a name="steanecodeencoderimpl-operation"></a><span data-ttu-id="b2b1f-102">Steanecodeencoderimpl-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b2b1f-102">SteaneCodeEncoderImpl operation</span></span>

<span data-ttu-id="b2b1f-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="b2b1f-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="b2b1f-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b2b1f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b2b1f-105">Der private Vorgang, der verwendet wird, um sowohl den Steane-Code Encoder als auch den Decoder</span><span class="sxs-lookup"><span data-stu-id="b2b1f-105">Private operation used to implement both the Steane code encoder and decoder.</span></span>

```qsharp
operation SteaneCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="b2b1f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="b2b1f-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="b2b1f-107">Daten: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b2b1f-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b2b1f-108">ein Array mit einem Qubit, das das Eingabe-Qubit ist.</span><span class="sxs-lookup"><span data-stu-id="b2b1f-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="b2b1f-109">Scratch: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b2b1f-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b2b1f-110">ein Array mit 6 Qubits, die Redundanz hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b2b1f-110">an array holding 6 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b2b1f-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b2b1f-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

