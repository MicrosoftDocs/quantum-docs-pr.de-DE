---
title: Mathematik in den Q# Standardbibliotheken
description: Erfahren Sie mehr über die klassischen mathematischen Funktionen in den Q# Standardbibliotheken, die mit den integrierten Datentypen verwendet werden.
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad
ms.topic: article
no-loc:
- Q#
- $$v
ms.openlocfilehash: 55b1ef70eed1eb47ab0c6b30e2b8203c38c9a67a
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/21/2020
ms.locfileid: "90833598"
---
# <a name="classical-mathematical-functions"></a>Klassische mathematische Funktionen #

Diese Funktionen werden hauptsächlich verwendet, um mit den Q# integrierten Datentypen, und zu arbeiten `Int` `Double` `Range` .

Der <xref:microsoft.quantum.intrinsic.random> Vorgang hat eine Signatur `(Double[] => Int)` .
Er nimmt ein Array von Double-Eingaben als Eingabe und gibt einen zufällig ausgewählten Index als ein an das Array zurück `Int` .
Die Wahrscheinlichkeit für die Auswahl eines bestimmten Indexes ist proportional zum Wert des Array Elements an diesem Index. n Array Elemente, die gleich 0 (null) sind, werden ignoriert, und ihre Indizes werden nie zurückgegeben.
Wenn ein Array Element kleiner als 0 (null) ist, oder wenn kein Array Element größer als 0 (null) ist, schlägt der Vorgang fehl.
