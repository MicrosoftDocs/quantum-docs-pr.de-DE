---
uid: Microsoft.Quantum.MachineLearning.FeatureRegisterSize
title: Featureregistersize-Funktion
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: FeatureRegisterSize
qsharp.summary: Returns the number of qubits required to encode a particular feature vector.
ms.openlocfilehash: 8f7c47c7547e7a0ac1672f308de445c1b46461e1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92723284"
---
# <a name="featureregistersize-function"></a><span data-ttu-id="afcfb-102">Featureregistersize-Funktion</span><span class="sxs-lookup"><span data-stu-id="afcfb-102">FeatureRegisterSize function</span></span>

<span data-ttu-id="afcfb-103">Namespace: [Microsoft. Quantum. machinelearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="afcfb-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="afcfb-104">Paketen [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="afcfb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="afcfb-105">Gibt die Anzahl von Qubits zurück, die erforderlich sind, um einen bestimmten featurevektor zu codieren.</span><span class="sxs-lookup"><span data-stu-id="afcfb-105">Returns the number of qubits required to encode a particular feature vector.</span></span>

```qsharp
function FeatureRegisterSize (sample : Double[]) : Int
```


## <a name="input"></a><span data-ttu-id="afcfb-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="afcfb-106">Input</span></span>

### <a name="sample--double"></a><span data-ttu-id="afcfb-107">Beispiel: [Double](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="afcfb-107">sample : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="afcfb-108">Ein Beispiel Funktions Vektor, der in ein Qubit-Register codiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="afcfb-108">A sample feature vector to be encoded into a qubit register.</span></span>



## <a name="output--int"></a><span data-ttu-id="afcfb-109">Ausgabe: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="afcfb-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="afcfb-110">Die zum Codieren `sample` in ein Qubit-Register erforderliche Größe, ausgedrückt als Anzahl von Qubits.</span><span class="sxs-lookup"><span data-stu-id="afcfb-110">The size required to encode `sample` into a qubit register, expressed as a number of qubits.</span></span>