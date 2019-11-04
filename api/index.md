---
uid: microsoft.quantum.standardlibsintro
title: Q#-Standardbibliothek für Microsoft Quantum
description: Referenzdokumentation zur Q#-Standardbibliothek für Microsoft Quantum
author: natke
ms.author: nakersha
ms.date: 09/04/2019
ms.topic: landing-page
ms.openlocfilehash: 25a53e1cb8577761ef89cdcf2cfcddc509093f86
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/29/2019
ms.locfileid: "73056964"
---
# <a name="q-standard-libraries"></a><span data-ttu-id="a08e7-103">Q#-Standardbibliotheken</span><span class="sxs-lookup"><span data-stu-id="a08e7-103">Q# standard libraries</span></span> #

<span data-ttu-id="a08e7-104">Q# wird durch eine Reihe nützlicher Vorgänge, Funktionen und benutzerdefinierter Typen unterstützt, die in der Q#-*Standardbibliothek* enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="a08e7-104">Q# is supported by a range of different useful operations, functions, and user-defined types that comprise the Q# *standard library*.</span></span>
<span data-ttu-id="a08e7-105">Die Q#-Standardbibliothek ist in zwei Hauptbereiche unterteilt:</span><span class="sxs-lookup"><span data-stu-id="a08e7-105">The Q# standard library is split into two main parts:</span></span>

- <span data-ttu-id="a08e7-106">**Einleitung**: Vorgänge und Funktionen, die als Teil des Zielcomputers und Compilers definiert und normalerweise in klassischem nativen .NET-Code geschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="a08e7-106">**The prelude**: operations and functions defined as a part of the target machine and compiler, typically in classical native .NET code.</span></span>
  <span data-ttu-id="a08e7-107">Im Allgemeinen verfügen unterschiedliche Zielcomputer ggf. über unterschiedliche Implementierungen der Einleitung, die für das jeweilige System entsprechend geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="a08e7-107">In general, different target machines may have different implementations of the prelude appropriate to each system.</span></span>
- <span data-ttu-id="a08e7-108">**Grundsätze**: Vorgänge und Funktionen als Q#-Definition, mit denen die Logik der Einleitung erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="a08e7-108">**The canon**: operations and functions defined in Q# building on the logic defined in the prelude.</span></span>
  <span data-ttu-id="a08e7-109">Die Implementierung der Grundsätze ist in Bezug auf Zielcomputer agnostisch.</span><span class="sxs-lookup"><span data-stu-id="a08e7-109">The canon implementation is agnostic with respect to target machines.</span></span>
<span data-ttu-id="a08e7-110">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span><span class="sxs-lookup"><span data-stu-id="a08e7-110">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;</span></span>