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
# <a name="classical-mathematical-functions"></a>Klassische mathematische Funktionen #

Diese Funktionen werden hauptsächlich verwendet, um mit den Q# integrierten Datentypen, und zu arbeiten `Int` `Double` `Range` .

Der <xref:Microsoft.Quantum.Intrinsic.Random> Vorgang hat eine Signatur `(Double[] => Int)` .
Er nimmt ein Array von Double-Eingaben als Eingabe und gibt einen zufällig ausgewählten Index als ein an das Array zurück `Int` .
Die Wahrscheinlichkeit für die Auswahl eines bestimmten Indexes ist proportional zum Wert des Array Elements an diesem Index. n Array Elemente, die gleich 0 (null) sind, werden ignoriert, und ihre Indizes werden nie zurückgegeben.
Wenn ein Array Element kleiner als 0 (null) ist, oder wenn kein Array Element größer als 0 (null) ist, schlägt der Vorgang fehl.
