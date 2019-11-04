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
# <a name="classical-mathematical-functions"></a>Klassische mathematische Funktionen #

Diese Funktionen werden hauptsächlich verwendet, um mit den integrierten f #-Datentypen `Int`, `Double`und `Range`zu arbeiten.

Der <xref:microsoft.quantum.intrinsic.random> Vorgang verfügt über eine Signatur `(Double[] => Int)`.
Er nimmt ein Array von Doubles als Eingabe an und gibt einen zufällig ausgewählten Index als `Int`in das Array zurück.
Die Wahrscheinlichkeit für die Auswahl eines bestimmten Indexes ist proportional zum Wert des Array Elements an diesem Index. n Array Elemente, die gleich 0 (null) sind, werden ignoriert, und ihre Indizes werden nie zurückgegeben.
Wenn ein Array Element kleiner als 0 (null) ist, oder wenn kein Array Element größer als 0 (null) ist, schlägt der Vorgang fehl.