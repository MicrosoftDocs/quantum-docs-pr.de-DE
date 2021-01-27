---
uid: Microsoft.Quantum.Characterization.QuantumPhaseEstimation
title: Quantrephaseschätzungsvorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Characterization
qsharp.name: QuantumPhaseEstimation
qsharp.summary: Performs the quantum phase estimation algorithm for a given oracle `U` and `targetState`, reading the phase into a big-endian quantum register.
ms.openlocfilehash: 4bdf3de9dab20fa97ba47f15efec4b41a10709f3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98839662"
---
# <a name="quantumphaseestimation-operation"></a><span data-ttu-id="ce62d-102">Quantrephaseschätzungsvorgang</span><span class="sxs-lookup"><span data-stu-id="ce62d-102">QuantumPhaseEstimation operation</span></span>

<span data-ttu-id="ce62d-103">Namespace: [Microsoft. Quantum. Charakterisierung](xref:Microsoft.Quantum.Characterization)</span><span class="sxs-lookup"><span data-stu-id="ce62d-103">Namespace: [Microsoft.Quantum.Characterization](xref:Microsoft.Quantum.Characterization)</span></span>

<span data-ttu-id="ce62d-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ce62d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ce62d-105">Führt den Algorithmus für die Quantum-Phasen Schätzung für ein bestimmtes Oracle `U` und aus `targetState` , wobei die Phase in ein Big-in-Quantum-Quantum-Register gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="ce62d-105">Performs the quantum phase estimation algorithm for a given oracle `U` and `targetState`, reading the phase into a big-endian quantum register.</span></span>

```qsharp
operation QuantumPhaseEstimation (oracle : Microsoft.Quantum.Oracles.DiscreteOracle, targetState : Qubit[], controlRegister : Microsoft.Quantum.Arithmetic.BigEndian) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="ce62d-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="ce62d-106">Input</span></span>

### <a name="oracle--discreteoracle"></a><span data-ttu-id="ce62d-107">Oracle: [diskreteoracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span><span class="sxs-lookup"><span data-stu-id="ce62d-107">oracle : [DiscreteOracle](xref:Microsoft.Quantum.Oracles.DiscreteOracle)</span></span>

<span data-ttu-id="ce62d-108">Ein Vorgang, der $U ^ m $ für die angegebenen ganzzahligen Kräfte m implementiert.</span><span class="sxs-lookup"><span data-stu-id="ce62d-108">An operation implementing $U^m$ for given integer powers m.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="ce62d-109">targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="ce62d-109">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="ce62d-110">Ein Quantum-Register, das den Status $ \ket{\phi} $ darstellt, der durch $U $ bearbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="ce62d-110">A quantum register representing the state $\ket{\phi}$ acted on by $U$.</span></span> <span data-ttu-id="ce62d-111">Wenn $ \ket{\phi} $ ein eigen Status von $U $ ist, $U \ket{\phi} = e ^ {i\phi} \ket{\phi} $ für $ \phi \in [0,0 \ PI) $ eine unbekannte Phase.</span><span class="sxs-lookup"><span data-stu-id="ce62d-111">If $\ket{\phi}$ is an eigenstate of $U$, $U\ket{\phi} = e^{i\phi} \ket{\phi}$ for $\phi \in [0, 2\pi)$ an unknown phase.</span></span>


### <a name="controlregister--bigendian"></a><span data-ttu-id="ce62d-112">controlregister: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="ce62d-112">controlRegister : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="ce62d-113">Ein ganzzahliges Register für eine Big-Endian-Darstellung, das verwendet werden kann, um das angegebene Oracle zu steuern, und das eine Darstellung von $ \phi $ nach der Anwendung dieses Vorgangs enthält.</span><span class="sxs-lookup"><span data-stu-id="ce62d-113">A big-endian representation integer register that can be used to control the provided oracle, and that will contain the a representation of $\phi$ following the application of this operation.</span></span> <span data-ttu-id="ce62d-114">Es wird davon ausgegangen, dass das controlregister im ursprünglichen Zustand $ \ket{00\cdots 0} $ beginnt, wobei die Länge des Registers die gewünschte Genauigkeit angibt.</span><span class="sxs-lookup"><span data-stu-id="ce62d-114">The controlRegister is assumed to start in the initial state $\ket{00\cdots 0}$, where the length of the register indicates the desired precision.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ce62d-115">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ce62d-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

