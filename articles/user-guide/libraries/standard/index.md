---
title: Einführung in Q#-Standardbibliotheken von Microsoft
description: Hier finden Sie Informationen zu den Q#-Standardbibliotheken von Microsoft, mit denen die Vorgänge, Funktionen und Datentypen definiert werden, die in Quantenprogrammen zum Einsatz kommen.
author: QuantumWriter
ms.author: martinro
ms.date: 12/11/2017
ms.topic: conceptual
uid: microsoft.quantum.libraries.standard.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 58e271fefba84e45c5558eeee066bc37c22bf63b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858317"
---
# <a name="introduction-to-the-no-locq-standard-libraries"></a>Einführung in die Q#-Standardbibliotheken

Q# wird von verschiedenen praktischen Vorgängen, Funktionen und benutzerdefinierten Typen unterstützt, die die Q#-*Standardbibliotheken* umfassen.
Das bei der [Installation und Überprüfung](xref:microsoft.quantum.install) installierte [`Microsoft.Quantum.Development.Kit`-NuGet-Paket](https://www.nuget.org/packages/microsoft.quantum.development.kit) stellt den Q#-Compiler sowie Teile der Standardbibliothek bereit, die vom Zielcomputer implementiert werden.
Das [`Microsoft.Quantum.Standard`-Paket](https://www.nuget.org/packages/microsoft.quantum.standard) stellt den Teil der Q#-Standardbibliotheken bereit, der auf mehrere Zielcomputer übertragbar ist.

Die durch die Q#-Standardbibliotheken definierten Symbole werden in der [API-Dokumentation](xref:microsoft.quantum.apiref-intro) wesentlich ausführlicher definiert.

In den folgenden Abschnitten werden die wichtigsten Funktionen der einzelnen Teile der Standardbibliothek beschrieben. Außerdem wird erläutert, wie die einzelnen Funktionen in der Praxis verwendet werden können.
