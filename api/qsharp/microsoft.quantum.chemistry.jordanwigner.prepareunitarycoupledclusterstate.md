---
uid: Microsoft.Quantum.Chemistry.JordanWigner.PrepareUnitaryCoupledClusterState
title: Prepareunitarycoupledclusterstate-Vorgang
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: PrepareUnitaryCoupledClusterState
qsharp.summary: Unitary coupled-cluster state preparation of trial state
ms.openlocfilehash: 1d5b8963bd50752fef22fea0a3c002e3e2ebc90a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98836048"
---
# <a name="prepareunitarycoupledclusterstate-operation"></a><span data-ttu-id="fb06f-102">Prepareunitarycoupledclusterstate-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fb06f-102">PrepareUnitaryCoupledClusterState operation</span></span>

<span data-ttu-id="fb06f-103">Namespace: [Microsoft. Quantum. Chemistry. jordanwigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="fb06f-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="fb06f-104">Paket: [Microsoft. Quantum. Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="fb06f-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="fb06f-105">Einheitlicher verknüpfter Cluster Status Vorbereitung des Test Zustands</span><span class="sxs-lookup"><span data-stu-id="fb06f-105">Unitary coupled-cluster state preparation of trial state</span></span>

```qsharp
operation PrepareUnitaryCoupledClusterState (initialStatePreparation : (Qubit[] => Unit), clusterOperator : Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState[], trotterStepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="fb06f-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="fb06f-106">Input</span></span>

### <a name="initialstatepreparation--qubit--unit"></a><span data-ttu-id="fb06f-107">initialstatepreparation: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fb06f-107">initialStatePreparation : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="fb06f-108">Einheitlich zum Vorbereiten des anfänglichen Test Zustands.</span><span class="sxs-lookup"><span data-stu-id="fb06f-108">Unitary to prepare initial trial state.</span></span>


### <a name="clusteroperator--jordanwignerinputstate"></a><span data-ttu-id="fb06f-109">clusteroperator: [jordanwignerinputstate](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span><span class="sxs-lookup"><span data-stu-id="fb06f-109">clusterOperator : [JordanWignerInputState](xref:Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerInputState)[]</span></span>




### <a name="trotterstepsize--double"></a><span data-ttu-id="fb06f-110">trotterstepsize: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fb06f-110">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>




### <a name="qubits--qubit"></a><span data-ttu-id="fb06f-111">Qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fb06f-111">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="fb06f-112">Qubits von hamiltonan.</span><span class="sxs-lookup"><span data-stu-id="fb06f-112">Qubits of Hamiltonian.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fb06f-113">Ausgabe: [Einheit](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fb06f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

