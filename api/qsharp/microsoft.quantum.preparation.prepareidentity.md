---
uid: Microsoft.Quantum.Preparation.PrepareIdentity
title: Prepareidentity-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareIdentity
qsharp.summary: >-
  Given a register, prepares that register in the maximally mixed state.

  The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.
ms.openlocfilehash: a3f96fbdafb19c90fb2b563243600cca60841566
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92724893"
---
# <a name="prepareidentity-operation"></a><span data-ttu-id="d0fb1-102">Prepareidentity-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d0fb1-102">PrepareIdentity operation</span></span>

<span data-ttu-id="d0fb1-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="d0fb1-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="d0fb1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d0fb1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d0fb1-105">Bereitet bei einem Register das registrieren im Status "maximisch" vor.</span><span class="sxs-lookup"><span data-stu-id="d0fb1-105">Given a register, prepares that register in the maximally mixed state.</span></span>

<span data-ttu-id="d0fb1-106">Das Register wird im Zustand $ \boldone/2 ^ N $ vorbereitet, indem der gesamte depolarisierungschannel auf die einzelnen Qubits angewendet wird, wobei $N $ die Länge des Registers ist.</span><span class="sxs-lookup"><span data-stu-id="d0fb1-106">The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.</span></span>

```qsharp
operation PrepareIdentity (register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d0fb1-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d0fb1-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="d0fb1-108">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d0fb1-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d0fb1-109">Ein Register, dessen Zustand in der oben beschriebenen Weise depolarisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d0fb1-109">A register whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d0fb1-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d0fb1-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="d0fb1-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d0fb1-111">See Also</span></span>

- [<span data-ttu-id="d0fb1-112">Microsoft. Quantum. Preparation. preparesinglequbitidentity</span><span class="sxs-lookup"><span data-stu-id="d0fb1-112">Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity</span></span>](xref:Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity)