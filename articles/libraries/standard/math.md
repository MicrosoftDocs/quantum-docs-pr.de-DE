---
title: 'Math in den Q # Standard-Bibliotheken'
description: 'Erfahren Sie mehr über die klassischen mathematischen Funktionen in den Q # Standard-Bibliotheken, die mit den integrierten Datentypen verwendet werden.'
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: bec866472abc0d4327cdc570306341375395f492
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906150"
---
# <a name="classical-mathematical-functions"></a><span data-ttu-id="cb7fa-103">Klassische mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="cb7fa-103">Classical Mathematical Functions</span></span> #

<span data-ttu-id="cb7fa-104">Diese Funktionen werden hauptsächlich verwendet, um mit den integrierten f #-Datentypen `Int`, `Double`und `Range`zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cb7fa-104">These functions are primarily used to work with the Q# built-in data types `Int`, `Double`, and `Range`.</span></span>

<span data-ttu-id="cb7fa-105">Der <xref:microsoft.quantum.intrinsic.random> Vorgang verfügt über eine Signatur `(Double[] => Int)`.</span><span class="sxs-lookup"><span data-stu-id="cb7fa-105">The <xref:microsoft.quantum.intrinsic.random> operation has signature `(Double[] => Int)`.</span></span>
<span data-ttu-id="cb7fa-106">Er nimmt ein Array von Doubles als Eingabe an und gibt einen zufällig ausgewählten Index als `Int`in das Array zurück.</span><span class="sxs-lookup"><span data-stu-id="cb7fa-106">It takes an array of doubles as input, and returns a randomly-selected index into the array as an `Int`.</span></span>
<span data-ttu-id="cb7fa-107">Die Wahrscheinlichkeit für die Auswahl eines bestimmten Indexes ist proportional zum Wert des Array Elements an diesem Index.</span><span class="sxs-lookup"><span data-stu-id="cb7fa-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span> <span data-ttu-id="cb7fa-108">n Array Elemente, die gleich 0 (null) sind, werden ignoriert, und ihre Indizes werden nie zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cb7fa-108">n Array elements that are equal to zero are ignored and their indices are never returned.</span></span>
<span data-ttu-id="cb7fa-109">Wenn ein Array Element kleiner als 0 (null) ist, oder wenn kein Array Element größer als 0 (null) ist, schlägt der Vorgang fehl.</span><span class="sxs-lookup"><span data-stu-id="cb7fa-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>
