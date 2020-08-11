---
title: Einführung in Q#-Standardbibliotheken von Microsoft
description: Hier finden Sie Informationen zu den Q#-Standardbibliotheken von Microsoft, mit denen die Vorgänge, Funktionen und Datentypen definiert werden, die in Quantenprogrammen zum Einsatz kommen.
author: QuantumWriter
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.libraries.standard.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 4db227fcf159331f9f8456c474ce6d64111c21df
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868473"
---
# <a name="introduction-to-the-no-locq-standard-libraries"></a>Einführung in die Q#-Standardbibliotheken

Q# wird von verschiedenen praktischen Vorgängen, Funktionen und benutzerdefinierten Typen unterstützt, die die Q#-*Standardbibliotheken* umfassen.
Das bei der [Installation und Überprüfung](xref:microsoft.quantum.install) installierte [`Microsoft.Quantum.Development.Kit`-NuGet-Paket](https://www.nuget.org/packages/microsoft.quantum.development.kit) stellt den Q#-Compiler sowie Teile der Standardbibliothek bereit, die vom Zielcomputer implementiert werden.
Das [`Microsoft.Quantum.Standard`-Paket](https://www.nuget.org/packages/microsoft.quantum.standard) stellt den Teil der Q#-Standardbibliotheken bereit, der auf mehrere Zielcomputer übertragbar ist.

Die durch die Q#-Standardbibliotheken definierten Symbole werden in der [API-Dokumentation](xref:microsoft.quantum.standardlibsintro) wesentlich ausführlicher definiert.

In den folgenden Abschnitten werden die wichtigsten Funktionen der einzelnen Teile der Standardbibliothek beschrieben. Außerdem wird erläutert, wie die einzelnen Funktionen in der Praxis verwendet werden können.
