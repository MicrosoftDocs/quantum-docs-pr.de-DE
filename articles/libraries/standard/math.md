---
title: 'Q # Standard-Bibliotheken-math | Microsoft-Dokumentation'
description: 'F #-Standardbibliotheken-math'
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: 7ac9d321f59f7cc95ad8939a4cf7c36e0c5e0491
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2019
ms.locfileid: "73184456"
---
# <a name="classical-mathematical-functions"></a><span data-ttu-id="92300-103">Klassische mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="92300-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="92300-104">Diese Funktionen werden hauptsächlich verwendet, um mit den integrierten f #-Datentypen `Int`, `Double`und `Range`zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="92300-104">These functions are primarily used to work with the Q# built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="92300-105">Der <xref:microsoft.quantum.intrinsic.random> Vorgang verfügt über eine Signatur `(Double[] => Int)`.</span><span class="sxs-lookup"><span data-stu-id="92300-105">The <xref:microsoft.quantum.intrinsic.random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="92300-106">Er nimmt ein Array von Doubles als Eingabe an und gibt einen zufällig ausgewählten Index als `Int`in das Array zurück.</span><span class="sxs-lookup"><span data-stu-id="92300-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="92300-107">Die Wahrscheinlichkeit für die Auswahl eines bestimmten Indexes ist proportional zum Wert des Array Elements an diesem Index.</span><span class="sxs-lookup"><span data-stu-id="92300-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="92300-108">n Array Elemente, die gleich 0 (null) sind, werden ignoriert, und ihre Indizes werden nie zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="92300-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="92300-109">Wenn ein Array Element kleiner als 0 (null) ist, oder wenn kein Array Element größer als 0 (null) ist, schlägt der Vorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="92300-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>