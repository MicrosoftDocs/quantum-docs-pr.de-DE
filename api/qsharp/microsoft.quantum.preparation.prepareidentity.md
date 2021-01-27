---
uid: Microsoft.Quantum.Preparation.PrepareIdentity
title: Prepareidentity-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareIdentity
qsharp.summary: >-
  Given a register, prepares that register in the maximally mixed state.

  The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.
ms.openlocfilehash: ec7e813110ccd9e6d499fc469fa27249a182b870
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855877"
---
# <a name="prepareidentity-operation"></a><span data-ttu-id="d3f4b-102">Prepareidentity-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d3f4b-102">PrepareIdentity operation</span></span>

<span data-ttu-id="d3f4b-103">Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)</span><span class="sxs-lookup"><span data-stu-id="d3f4b-103">Namespace: [Microsoft.Quantum.Preparation](xref:Microsoft.Quantum.Preparation)</span></span>

<span data-ttu-id="d3f4b-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d3f4b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d3f4b-105">Bereitet bei einem Register das registrieren im Status "maximisch" vor.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-105">Given a register, prepares that register in the maximally mixed state.</span></span>

<span data-ttu-id="d3f4b-106">Das Register wird im Zustand $ \boldone/2 ^ N $ vorbereitet, indem der gesamte depolarisierungschannel auf die einzelnen Qubits angewendet wird, wobei $N $ die Länge des Registers ist.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-106">The register is prepared in the $\boldone / 2^N$ state by applying the complete depolarizing channel to each qubit, where $N$ is the length of the register.</span></span>

```qsharp
operation PrepareIdentity (register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d3f4b-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d3f4b-107">Input</span></span>

### <a name="register--qubit"></a><span data-ttu-id="d3f4b-108">Register: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d3f4b-108">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d3f4b-109">Ein Register, dessen Zustand in der oben beschriebenen Weise depolarisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3f4b-109">A register whose state is to be depolarized in the manner described above.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d3f4b-110">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d3f4b-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="d3f4b-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d3f4b-111">See Also</span></span>

- [<span data-ttu-id="d3f4b-112">Microsoft. Quantum. Preparation. preparesinglequbitidentity</span><span class="sxs-lookup"><span data-stu-id="d3f4b-112">Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity</span></span>](xref:Microsoft.Quantum.Preparation.PrepareSingleQubitIdentity)