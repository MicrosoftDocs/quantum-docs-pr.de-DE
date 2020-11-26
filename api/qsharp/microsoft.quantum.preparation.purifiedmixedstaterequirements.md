---
uid: Microsoft.Quantum.Preparation.PurifiedMixedStateRequirements
title: Purifedmixedstatuerequirequirements-Funktion
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PurifiedMixedStateRequirements
qsharp.summary: Returns the total number of qubits that must be allocated in order to apply the operation returned by @"microsoft.quantum.preparation.purifiedmixedstate".
ms.openlocfilehash: 9b8861a4112c4e6c9db994339353c771a3de81a6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229986"
---
# <a name="purifiedmixedstaterequirements-function"></a>Purifedmixedstatuerequirequirements-Funktion

Namespace: [Microsoft. Quantum. Preparation](xref:Microsoft.Quantum.Preparation)

Paket: [Microsoft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gibt die Gesamtzahl der Qubits zurück, die zugeordnet werden müssen, um den von zurückgegebenen Vorgang anzuwenden @"microsoft.quantum.preparation.purifiedmixedstate" .

```qsharp
function PurifiedMixedStateRequirements (targetError : Double, nCoefficients : Int) : Microsoft.Quantum.Preparation.MixedStatePreparationRequirements
```


## <a name="input"></a>Eingabe

### <a name="targeterror--double"></a>targeterror: [Double](xref:microsoft.quantum.lang-ref.double)

Der Ziel Fehler $ \epsilon $.


### <a name="ncoefficients--int"></a>nkoeffizienten: [int](xref:microsoft.quantum.lang-ref.int)

Die Anzahl der Koeffizienten, die beim Vorbereiten eines gemischten Zustands angegeben werden sollen.



## <a name="output--mixedstatepreparationrequirements"></a>Ausgabe: [mixedstatepreparationrequirements](xref:Microsoft.Quantum.Preparation.MixedStatePreparationRequirements)

Eine Beschreibung, wie viele Qubits insgesamt erforderlich sind, und für jeden Index und die von der Funktion verwendeten Garbage Registern @"microsoft.quantum.preparation.purifiedmixedstate" .

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. Preparation. purifedmixedstate](xref:Microsoft.Quantum.Preparation.PurifiedMixedState)