---
uid: Microsoft.Quantum.Canon.RAll1
title: RAll1-Vorgang
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RAll1
qsharp.summary: >-
  Performs a phase shift operation.

  $R=\boldone-(1-e^{i \phi})\ket{1\cdots 1}\bra{1\cdots 1}$.
ms.openlocfilehash: 45892f9811faf56d7b9a0eb34e4bde0a32d5586d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703890"
---
# <a name="rall1-operation"></a><span data-ttu-id="d33b1-102">RAll1-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d33b1-102">RAll1 operation</span></span>

<span data-ttu-id="d33b1-103">Namespace: [Microsoft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d33b1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d33b1-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d33b1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d33b1-105">Führt einen Phasen Verschiebungs Vorgang aus.</span><span class="sxs-lookup"><span data-stu-id="d33b1-105">Performs a phase shift operation.</span></span>

<span data-ttu-id="d33b1-106">$R = \boldone-(1-e ^ {i \phi}) \ket{1\cdots 1} \bra{1\cdots 1} $.</span><span class="sxs-lookup"><span data-stu-id="d33b1-106">$R=\boldone-(1-e^{i \phi})\ket{1\cdots 1}\bra{1\cdots 1}$.</span></span>

```qsharp
operation RAll1 (phase : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d33b1-107">Eingabe</span><span class="sxs-lookup"><span data-stu-id="d33b1-107">Input</span></span>

### <a name="phase--double"></a><span data-ttu-id="d33b1-108">Phase: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d33b1-108">phase : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d33b1-109">Die Phase $ \phi $ wird auf den Status $ \ket{1\cdots 1} \bra{1\cdots 1} $ angewendet.</span><span class="sxs-lookup"><span data-stu-id="d33b1-109">The phase $\phi$ applied to state $\ket{1\cdots 1}\bra{1\cdots 1}$.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="d33b1-110">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d33b1-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d33b1-111">Das Register, dessen Zustand durch $R $ gedreht werden soll.</span><span class="sxs-lookup"><span data-stu-id="d33b1-111">The register whose state is to be rotated by $R$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d33b1-112">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d33b1-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

