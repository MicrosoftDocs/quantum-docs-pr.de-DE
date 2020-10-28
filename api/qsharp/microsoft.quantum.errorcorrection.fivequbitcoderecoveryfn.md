---
uid: Microsoft.Quantum.ErrorCorrection.FiveQubitCodeRecoveryFn
title: "\"Fvequbitcoderecoveryfn\"-Funktion"
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.ErrorCorrection
qsharp.name: FiveQubitCodeRecoveryFn
qsharp.summary: Returns function that maps error syndrome measurements to the appropriate error-correcting Pauli operators by table lookup for the ⟦5, 1, 3⟧ quantum code.
ms.openlocfilehash: 5b8afe222d197eb7d342ac45f027f2de9130b61a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702479"
---
# <a name="fivequbitcoderecoveryfn-function"></a>"Fvequbitcoderecoveryfn"-Funktion

Namespace: [Microsoft. Quantum. errorcorrection](xref:Microsoft.Quantum.ErrorCorrection)

Paketen [](https://nuget.org/packages/)


Gibt eine Funktion zurück, die Fehler-Syndrom-Messungen den entsprechenden Fehler Behebungs-Pauli-Operatoren durch die Tabellen Suche für den ⟦ 5, 1, 3 ⟧ Quantum-Code zuordnet.

```qsharp
function FiveQubitCodeRecoveryFn () : Microsoft.Quantum.ErrorCorrection.RecoveryFn
```


## <a name="output--recoveryfn"></a>Ausgabe: [Wiederherstellbarkeits-FN](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)

Funktion des Typs `RecoveryFn` , die eine Messungs Messung annimmt `Result[]` und die `Pauli[]` Operatoren zurückgibt, die den erkannten Fehler korrigieren.

## <a name="remarks"></a>Hinweise

Durch das Durchlaufen aller Fehler der Gewichtung $1 $ erhalten wir eine Summe von insgesamt $3 \ mal 5 = 15 $ möglichen nicht trivialen syndromes.
In Verbindung mit der Identität wird eine Fehler Tabelle und ein entsprechendes-Syndrom erstellt. Für den 5-Qubit-Code, der für diese Tabelle angegeben ist: $X \_ 1: (0, 0, 0, 1); X \_ 2: (1, 0, 0, 0); X \_ 3: (1, 1, 0, 0); X \_ 4: (0, 1, 1, 0); X \_ 5: (0,0, 1, 1) $, $Z \_ 1: (1, 0, 1, 0); Z \_ 2: (0, 1, 0, 1); Z \_ 3: (0,0, 1, 0); Z \_ 4: (1, 0, 0, 1); Z \_ 5: (0, 1, 0, 0) $ mit $Y _I $ durch Hinzufügen der $X _I $ und $Z _I $-Syndrome abgerufen werden. Beachten Sie, dass die Reihenfolge in der Wiederherstellung der Tabellen Suche angegeben wird, indem die bitvektoren in ganze Zahlen (mit Little Endian) umgerechnet werden.

## <a name="see-also"></a>Weitere Informationen

- [Microsoft. Quantum. errorcorrection. wiederherstellungfn](xref:Microsoft.Quantum.ErrorCorrection.RecoveryFn)