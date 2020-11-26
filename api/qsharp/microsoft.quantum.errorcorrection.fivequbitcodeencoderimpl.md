---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeEncoderImpl
title: Vorgang "mevequbitcodeencoderimpl"
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeEncoderImpl
qsharp.summary: Private operation used to implement both the 5 qubit encoder and decoder.
ms.openlocfilehash: f70d2d1352c7b2eebee7a863eba97d78d7351dab
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96200848"
---
# <a name="fivequbitcodeencoderimpl-operation"></a><span data-ttu-id="d908e-102">Vorgang "mevequbitcodeencoderimpl"</span><span class="sxs-lookup"><span data-stu-id="d908e-102">FiveQubitCodeEncoderImpl operation</span></span>

<span data-ttu-id="d908e-103">Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)</span><span class="sxs-lookup"><span data-stu-id="d908e-103">Namespace: [Microsoft.Quantum.ErrorCorrection](xref:Microsoft.Quantum.ErrorCorrection)</span></span>

<span data-ttu-id="d908e-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d908e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d908e-105">Privater Vorgang, der zum Implementieren des 5-Qubit-Encoders und-Decoders verwendet wird</span><span class="sxs-lookup"><span data-stu-id="d908e-105">Private operation used to implement both the 5 qubit encoder and decoder.</span></span>

```qsharp
operation FiveQubitCodeEncoderImpl (data : Qubit[], scratch : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="d908e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d908e-106">Input</span></span>

### <a name="data--qubit"></a><span data-ttu-id="d908e-107">Daten: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d908e-107">data : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d908e-108">ein Array mit einem Qubit, das das Eingabe-Qubit ist.</span><span class="sxs-lookup"><span data-stu-id="d908e-108">an array holding 1 qubit which is the input qubit.</span></span>


### <a name="scratch--qubit"></a><span data-ttu-id="d908e-109">Scratch: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d908e-109">scratch : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d908e-110">ein Array mit vier Qubits, die Redundanz hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d908e-110">an array holding 4 qubits which add redundancy.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d908e-111">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d908e-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d908e-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d908e-112">Remarks</span></span>

<span data-ttu-id="d908e-113">Der ausgewählte Encoder stammt aus dem Papier V. kliuchnikov und D. Maslov, "Optimierung von Clifford-Leitungen", Phys. Rev. Phys. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Abbildung 4B) und erfordert insgesamt 11 Gates.</span><span class="sxs-lookup"><span data-stu-id="d908e-113">The particular encoder chosen was taken from the paper V. Kliuchnikov and D. Maslov, "Optimization of Clifford Circuits," Phys. Rev. Phys. Rev. A 88, 052307 (2013); https://arxiv.org/abs/1305.0810, Figure 4b) and requires a total of 11 gates.</span></span>