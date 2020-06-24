---
title: 'Math in den Q # Standard-Bibliotheken'
description: 'Erfahren Sie mehr über die klassischen mathematischen Funktionen in den Q # Standard-Bibliotheken, die mit den integrierten Datentypen verwendet werden.'
author: cgranade
uid: microsoft.quantum.libraries.math
ms.author: chgranad@microsoft.com
ms.topic: article
ms.openlocfilehash: bec866472abc0d4327cdc570306341375395f492
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274956"
---
# <a name="classical-mathematical-functions"></a>Klassische mathematische Funktionen #

Diese Funktionen werden hauptsächlich verwendet, um mit den integrierten f #-Datentypen `Int` , `Double` und zu arbeiten `Range` .

Der <xref:microsoft.quantum.intrinsic.random> Vorgang hat eine Signatur `(Double[] => Int)` .
Er nimmt ein Array von Double-Eingaben als Eingabe und gibt einen zufällig ausgewählten Index als ein an das Array zurück `Int` .
Die Wahrscheinlichkeit für die Auswahl eines bestimmten Indexes ist proportional zum Wert des Array Elements an diesem Index. n Array Elemente, die gleich 0 (null) sind, werden ignoriert, und ihre Indizes werden nie zurückgegeben.
Wenn ein Array Element kleiner als 0 (null) ist, oder wenn kein Array Element größer als 0 (null) ist, schlägt der Vorgang fehl.
