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
# <a name="classical-mathematical-functions"></a>Klassische mathematische Funktionen #

Diese Funktionen werden hauptsächlich verwendet, um mit den integrierten f #-Datentypen `Int`, `Double`und `Range`zu arbeiten.

Der <xref:microsoft.quantum.intrinsic.random> Vorgang verfügt über eine Signatur `(Double[] => Int)`.
Er nimmt ein Array von Doubles als Eingabe an und gibt einen zufällig ausgewählten Index als `Int`in das Array zurück.
Die Wahrscheinlichkeit für die Auswahl eines bestimmten Indexes ist proportional zum Wert des Array Elements an diesem Index. n Array Elemente, die gleich 0 (null) sind, werden ignoriert, und ihre Indizes werden nie zurückgegeben.
Wenn ein Array Element kleiner als 0 (null) ist, oder wenn kein Array Element größer als 0 (null) ist, schlägt der Vorgang fehl.
