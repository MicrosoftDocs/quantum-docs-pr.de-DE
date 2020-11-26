---
uid: Microsoft.Quantum.Preparation.PrepareIdentity
title: Prepareidentity-Vorgang
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareIdentity
qsharp.summary: >-
  Given a register, prepares that register in the maximally mixed state.

  The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.
ms.openlocfilehash: 6e0a43e61e3c49edef94db63f07ed29132d84c83
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210436"
---
# <a name="prepareidentity-operation"></a><span data-ttu-id="71274-102">Prepareidentity-Vorgang</span><span class="sxs-lookup"><span data-stu-id="71274-102">PrepareIdentity operation</span></span>

<span data-ttu-id="71274-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="71274-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="71274-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="71274-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="71274-105">Bereitet bei einem Register das registrieren im Status "maximisch" vor.</span><span class="sxs-lookup"><span data-stu-id="71274-105">Given a register, prepares that register in the maximally mixed state.</span></span>

<span data-ttu-id="71274-106">Das Register wird im Zustand $ \boldone/2 ^ N $ vorbereitet, indem der gesamte depolarisierungschannel auf die einzelnen Qubits angewendet wird, wobei $N $ die Länge des Registers ist.</span><span class="sxs-lookup"><span data-stu-id="71274-106">The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.</span></span>

```qsharp
operation PrepareIdentity (register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="71274-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="71274-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="71274-108">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="71274-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="71274-109">Ein Register, dessen Zustand in der oben beschriebenen Weise depolarisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="71274-109">A register whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="71274-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="71274-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="71274-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="71274-111">See Also</span></span>

- [<span data-ttu-id="71274-112">Microsoft. Quantum. Preparation. preparesinglequbitidentity</span><span class="sxs-lookup"><span data-stu-id="71274-112">Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity</span></span>](xref:Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity)