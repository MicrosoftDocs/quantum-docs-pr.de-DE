---
uid: Microsoft.Quantum.Arithmetic.BigEndianAsLittleEndian
title: Bigendianaslittleendian-Funktion
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: BigEndianAsLittleEndian
qsharp.summary: Converts a `BigEndian` qubit register to a `LittleEndian` qubit register by reversing the qubit ordering.
ms.openlocfilehash: cb4cf68753468952c7541fae23250ed1fd1914f9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843370"
---
# <a name="bigendianaslittleendian-function"></a><span data-ttu-id="90615-102">Bigendianaslittleendian-Funktion</span><span class="sxs-lookup"><span data-stu-id="90615-102">BigEndianAsLittleEndian function</span></span>

<span data-ttu-id="90615-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="90615-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="90615-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="90615-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="90615-105">Konvertiert ein `BigEndian` Qubit-Register in eine `LittleEndian` Qubit-Registrierung, indem die Qubit-Reihenfolge umgekehrt wird.</span><span class="sxs-lookup"><span data-stu-id="90615-105">Converts a `BigEndian` qubit register to a `LittleEndian` qubit register by reversing the qubit ordering.</span></span>

```qsharp
function BigEndianAsLittleEndian (input : Microsoft.Quantum.Arithmetic.BigEndian) : Microsoft.Quantum.Arithmetic.LittleEndian
```


## <a name="input"></a><span data-ttu-id="90615-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="90615-106">Input</span></span>

### <a name="input--bigendian"></a><span data-ttu-id="90615-107">Eingabe: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span><span class="sxs-lookup"><span data-stu-id="90615-107">input : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian)</span></span>

<span data-ttu-id="90615-108">Das Qubit-Register im- `BigEndian` Format.</span><span class="sxs-lookup"><span data-stu-id="90615-108">Qubit register in `BigEndian` format.</span></span>



## <a name="output--littleendian"></a><span data-ttu-id="90615-109">Ausgabe: [littleenddian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="90615-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="90615-110">Das Qubit-Register im- `LittleEndian` Format.</span><span class="sxs-lookup"><span data-stu-id="90615-110">Qubit register in `LittleEndian` format.</span></span>