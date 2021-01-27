---
title: Mathematik in den Q# Standardbibliotheken
description: Erfahren Sie mehr über die klassischen mathematischen Funktionen in den Q# Standardbibliotheken, die mit den integrierten Datentypen verwendet werden.
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad
ms.topic: conceptual
no-loc:
- Q#
- $$v
ms.openlocfilehash: a2e2656f42213c8ae9e984f63f3ebf4058520532
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853999"
---
# <a name="classical-mathematical-functions"></a><span data-ttu-id="ffffc-103">Klassische mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="ffffc-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="ffffc-104">Diese Funktionen werden hauptsächlich verwendet, um mit den Q# integrierten Datentypen, und zu arbeiten `Int` `Double` `Range` .</span><span class="sxs-lookup"><span data-stu-id="ffffc-104">These functions are primarily used to work with the Q# built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="ffffc-105">Der <xref:Microsoft.Quantum.Intrinsic.Random> Vorgang hat eine Signatur `(Double[] => Int)` .</span><span class="sxs-lookup"><span data-stu-id="ffffc-105">The <xref:Microsoft.Quantum.Intrinsic.Random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="ffffc-106">Er nimmt ein Array von Double-Eingaben als Eingabe und gibt einen zufällig ausgewählten Index als ein an das Array zurück `Int` .</span><span class="sxs-lookup"><span data-stu-id="ffffc-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="ffffc-107">Die Wahrscheinlichkeit für die Auswahl eines bestimmten Indexes ist proportional zum Wert des Array Elements an diesem Index.</span><span class="sxs-lookup"><span data-stu-id="ffffc-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="ffffc-108">n Array Elemente, die gleich 0 (null) sind, werden ignoriert, und ihre Indizes werden nie zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ffffc-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="ffffc-109">Wenn ein Array Element kleiner als 0 (null) ist, oder wenn kein Array Element größer als 0 (null) ist, schlägt der Vorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="ffffc-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>
