---
title: Einführung in Microsoft Q#-Standardbibliotheken
description: Enthält eine Beschreibung der Microsoft Q#-Standardbibliotheken, mit denen die Vorgänge, Funktionen und Datentypen definiert werden, die in Quantenprogrammen genutzt werden.
author: QuantumWriter
ms.author: martinro@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.libraries.standard.intro
ms.openlocfilehash: ab069c496d89a57f979732da6ccdfbe673b79726
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/21/2020
ms.locfileid: "86870582"
---
# <a name="introduction-to-the-q-standard-libraries"></a>Einführung in die Q#-Standardbibliotheken

Q# wird von einer Reihe nützlicher Vorgänge, Funktionen und benutzerdefinierten Typen unterstützt, die die *Q#-Standardbibliotheken* umfassen.
Das bei der [Installation und Überprüfung](xref:microsoft.quantum.install) installierte [`Microsoft.Quantum.Development.Kit`-NuGet-Paket](https://www.nuget.org/packages/microsoft.quantum.development.kit) stellt den Q#-Compiler sowie Teile der Standardbibliothek bereit, die vom Zielcomputer implementiert werden.
Das [`Microsoft.Quantum.Standard`-Paket](https://www.nuget.org/packages/microsoft.quantum.standard) stellt den Teil der Q#-Standardbibliotheken bereit, der auf mehrere Zielcomputer übertragbar ist.

Die durch die Q#-Standardbibliotheken definierten Symbole werden in der [API-Dokumentation](xref:microsoft.quantum.standardlibsintro) wesentlich ausführlicher definiert.

In den folgenden Abschnitten werden die wichtigsten Funktionen der einzelnen Teile der Standardbibliothek beschrieben. Außerdem wird erläutert, wie die einzelnen Funktionen in der Praxis verwendet werden können.
