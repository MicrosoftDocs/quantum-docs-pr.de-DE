---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedZ
title: _JWOptimizedZ Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedZ
qsharp.summary: Applies a Rz rotation, with a C-NOT trick to double phase in phase estimation.
ms.openlocfilehash: 8bbd4af0389a7b748be11dc50bacd2c178521adc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724628"
---
# <a name="_jwoptimizedz-operation"></a><span data-ttu-id="f63cf-102">_JWOptimizedZ Vorgang</span><span class="sxs-lookup"><span data-stu-id="f63cf-102">_JWOptimizedZ operation</span></span>

<span data-ttu-id="f63cf-103">Namespace: [Microsoft. Quantum. Research. Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="f63cf-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="f63cf-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f63cf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f63cf-105">Wendet eine RZ-Drehung mit einem C-not-Trick in eine doppelte Phase in der Phasen Schätzung an.</span><span class="sxs-lookup"><span data-stu-id="f63cf-105">Applies a Rz rotation, with a C-NOT trick to double phase in phase estimation.</span></span>

```qsharp
operation _JWOptimizedZ (angle : Double, parityQubit : Qubit, qubit : Qubit) : Unit
```


## <a name="input"></a><span data-ttu-id="f63cf-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f63cf-106">Input</span></span>

### <a name="angle--double"></a><span data-ttu-id="f63cf-107">Winkel: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f63cf-107">angle : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f63cf-108">Winkel der RZ-Drehung.</span><span class="sxs-lookup"><span data-stu-id="f63cf-108">Angle of Rz rotation.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="f63cf-109">parameteryqubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f63cf-109">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="f63cf-110">Qubit, das das Vorzeichen der Zeitentwicklung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f63cf-110">Qubit that determines the sign of time-evolution.</span></span>


### <a name="qubit--qubit"></a><span data-ttu-id="f63cf-111">Qubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="f63cf-111">qubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>





## <a name="output--unit"></a><span data-ttu-id="f63cf-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f63cf-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

