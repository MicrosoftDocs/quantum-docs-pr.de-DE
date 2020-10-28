---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoderImpl
title: Vorgang "mevequbitcodeencoderimpl"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeEncoderImpl
qsharp.summary: Private operation used to implement both the 5 qubit encoder and decoder.
ms.openlocfilehash: 29b0f47ddffeae3ed4dfda4084304427418e02fd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702480"
---
# <a name="fivequbitcodeencoderimpl-operation"></a><span data-ttu-id="91a55-102">Vorgang "mevequbitcodeencoderimpl"</span><span class="sxs-lookup"><span data-stu-id="91a55-102">FiveQubitCodeEncoderImpl operation</span></span>

<span data-ttu-id="91a55-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="91a55-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="91a55-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="91a55-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="91a55-105">Privater Vorgang, der zum Implementieren des 5-Qubit-Encoders und-Decoders verwendet wird</span><span class="sxs-lookup"><span data-stu-id="91a55-105">Private operation used to implement both the 5 qubit encoder and decoder.</span></span>

```qsharp
operation FiveQubitCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="91a55-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="91a55-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="91a55-107">Daten: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="91a55-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="91a55-108">ein Array mit einem Qubit, das das Eingabe-Qubit ist.</span><span class="sxs-lookup"><span data-stu-id="91a55-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="91a55-109">Scratch: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="91a55-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="91a55-110">ein Array mit vier Qubits, die Redundanz hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="91a55-110">an array holding 4 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="91a55-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="91a55-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="91a55-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="91a55-112">Remarks</span></span>

<span data-ttu-id="91a55-113">Der ausgewählte Encoder stammt aus dem Papier V. kliuchnikov und D. Maslov, "Optimierung von Clifford-Leitungen", Phys. Rev. Phys. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Abbildung 4B) und erfordert insgesamt 11 Gates.</span><span class="sxs-lookup"><span data-stu-id="91a55-113">The particular encoder chosen was taken from the paper V. Kliuchnikov and D. Maslov, "Optimization of Clifford Circuits," Phys. Rev. Phys. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Figure 4b) and requires a total of 11 gates.</span></span>