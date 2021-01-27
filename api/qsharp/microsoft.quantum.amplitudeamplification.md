---
uid: Microsoft.Quantum.AmplitudeAmplification
title: Microsoft. Quantum. amplitudebug-Namespace
ms.date: 1/23/2021 12:00:00 AM
ms.topic: managed-reference
qsharp.kind: namespace
qsharp.name: Microsoft.Quantum.AmplitudeAmplification
qsharp.summary: This namespace contains functions and operations for performing amplitude amplification.
ms.openlocfilehash: a014f923de62c5e660c1c0fc839fbe60e80f8ba9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845826"
---
# <a name="microsoftquantumamplitudeamplification-namespace"></a>Microsoft. Quantum. amplitudebug-Namespace

Dieser Namespace enthält Funktionen und Vorgänge zum Durchführen der Amplitude-Verstärkung.



## <a name="description"></a>Beschreibung

Eine schrägende Amplitude-Verstärkung mit partiellen Reflektionen ist die allgemeinste Form der hier implementierten Amplitude-Verstärkung.

Dies wird durch den Vorgang ampampobliviousbyreflectionphasen aufgerufen.

Dies hat zwei Register: `ancillaRegister` und `systemRegister` .

Dies akzeptiert zwei Oracles für diese Reflektionen des Typs `ReflectionOracle` , die nur für das `ancillaRegister` Register fungieren.

Dies akzeptiert eine Oracle-spezielle Verstärkung der Amplitude-Verstärkung des Typs `ObliviousOracle` , die zusammen für beide Register fungiert.

`ancillaRegister`Es wird davon ausgegangen, dass es sich bei dem Eingabe Status von um den eindeutigen $-$1-eigen Status des ersten reflektionsoperators handelt $I-2 \ Ket {s} \ Bra {s} $.

Reflektionen zu einem Ziel-Quantenzustand werden häufig implementiert, indem der Zugriff auf ein Oracle angenommen wird, das diesen Zustand von der Berechnungsbasis auf "$ \ket{0\cdots 0} $" vorbereitet.

Unsere Konvention für diese Oracles erfordert zwei Register: ein Single-Qubit- `flagQubit` Register und ein Register für alles andere auf dem Register "ancillaregister".

Das Oracle vom Typ `StateOracle` agiert gemeinsam in beiden Registern, um den Ziel Status zu erstellen, der durch $ \ket {1} $ im `flagQubit` Register mit einer echten Amplitude gekennzeichnet ist.

Die Reflektion `ReflectionOracle` über den Status dieses Flags wird durch den-Vorgang generiert `TargetStateReflectionOracle` .

Die Reflektion des `ReflectionOracle` Eingabe Zustands in `ancillaRegister` wird vom umgekehrten stateoracle generiert und dann über "$ \ket{0\cdots 0} $" mit reflectionstart () reflektiert.

Das Oracle vom Typ `DeterministicStateOracle` agiert in den `qubitState` Registern zum Erstellen des Ziel Zustands genau ohne Flag.

`AmpAmpObliviousByOraclePhases` eine Version der schrägen Amplitude-Verstärkung, die Oracles `StateOracle` und `ObliviousOracle` anstelle von Reflektionen akzeptiert.

Beachten Sie, dass die Amplitude-Verstärkung ein Sonderfall einer schrägen Amplitude-Verstärkung ist `ObliviousOracle` , wobei der Identitäts Operator ist und keine System-Qubits vorhanden sind, d.h., `systemRegister` ist leer.

Dies wird durch den-Vorgang `AmpAmByReflectionPhases` und den aufgerufen `AmpAmpByOraclePhases` .

Die Phasen für partielle Reflektionen im Standardfall der Grover-Suche werden von der Funktion ampampphasesstandard bereitgestellt.

Beispielsweise haben wir die folgenden Abhängigkeiten: ampampbyoracle-> ampampbyoraclephasen-> ampampobliviousbyoraclephasen-> ampampobliviousbyreflectionphasen.