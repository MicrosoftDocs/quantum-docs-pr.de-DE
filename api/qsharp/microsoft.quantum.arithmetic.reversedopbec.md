---
uid: Microsoft.Quantum.Arithmetic.ReversedOpBEC
title: Reversetdopbec-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: ReversedOpBEC
qsharp.summary: Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.
ms.openlocfilehash: 5bafe71b665eda082eafbe06be1308d6b042db2c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96222268"
---
# <a name="reversedopbec-function"></a><span data-ttu-id="1f99a-102">Reversetdopbec-Funktion</span><span class="sxs-lookup"><span data-stu-id="1f99a-102">ReversedOpBEC function</span></span>

<span data-ttu-id="1f99a-103">Namespace: [Microsoft. Quantum. Arithmetik](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="1f99a-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="1f99a-104">Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1f99a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1f99a-105">Gibt bei einem Vorgang, der eine Big-Endian-Eingabe annimmt, einen neuen Vorgang zurück, der eine Little-Endian-Eingabe annimmt.</span><span class="sxs-lookup"><span data-stu-id="1f99a-105">Given an operation that takes a big-endian input, returns a new operation that takes a little-endian input.</span></span>

```qsharp
function ReversedOpBEC (op : (Microsoft.Quantum.Arithmetic.BigEndian => Unit is Ctl)) : (Microsoft.Quantum.Arithmetic.LittleEndian => Unit is Ctl)
```


## <a name="input"></a><span data-ttu-id="1f99a-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="1f99a-106">Input</span></span>

### <a name="op--bigendian--unit--is-ctl"></a><span data-ttu-id="1f99a-107">OP: [bigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  ist CTL</span><span class="sxs-lookup"><span data-stu-id="1f99a-107">op : [BigEndian](xref:Microsoft.Quantum.Arithmetic.BigEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="1f99a-108">Der Vorgang, dessen Eingabe umgekehrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f99a-108">The operation whose input is to be reversed.</span></span>



## <a name="output--littleendian--unit--is-ctl"></a><span data-ttu-id="1f99a-109">Ausgabe: die [littleandian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) - => [Einheit](xref:microsoft.quantum.lang-ref.unit)  ist CTL.</span><span class="sxs-lookup"><span data-stu-id="1f99a-109">Output : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="1f99a-110">Ein neuer Vorgang, der seine Eingabe als Little-in-der-Register-Registrierung akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="1f99a-110">A new operation that accepts its input as a little-endian register.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f99a-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1f99a-111">See Also</span></span>

- [<span data-ttu-id="1f99a-112">Microsoft. Quantum. Arithmetik. applyrevertendopbec</span><span class="sxs-lookup"><span data-stu-id="1f99a-112">Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC</span></span>](xref:Microsoft.Quantum.Arithmetic.ApplyReversedOpBEC)
- [<span data-ttu-id="1f99a-113">Microsoft. Quantum. Arithmetik. revereindopbe</span><span class="sxs-lookup"><span data-stu-id="1f99a-113">Microsoft.Quantum.Arithmetic.ReversedOpBE</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBE)
- [<span data-ttu-id="1f99a-114">Microsoft. Quantum. Arithmetik. revereindopbea</span><span class="sxs-lookup"><span data-stu-id="1f99a-114">Microsoft.Quantum.Arithmetic.ReversedOpBEA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBEA)
- [<span data-ttu-id="1f99a-115">Microsoft. Quantum. Arithmetik. revereindopbeca</span><span class="sxs-lookup"><span data-stu-id="1f99a-115">Microsoft.Quantum.Arithmetic.ReversedOpBECA</span></span>](xref:Microsoft.Quantum.Arithmetic.ReversedOpBECA)