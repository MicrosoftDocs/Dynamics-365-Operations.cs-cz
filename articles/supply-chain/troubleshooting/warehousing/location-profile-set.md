---
title: Profil polohy vylučuje negativní zásoby, ale negativní zásoby k dispozici jsou povoleny
description: Možnost Povolit negativní zásoby pro profil umístění je nastavena na Ne, ale systém stále umožňuje negativní zásoby k dispozici.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 2a7345281301ee70a512dfadcd553cb4eb33003904d0dddf6967659b693f60d7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742601"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a>Profil polohy vylučuje negativní zásoby, ale negativní zásoby k dispozici jsou povoleny

Číslo článku znalostní báze: 4613622

## <a name="symptoms"></a>Příznaky

Možnost **Povolit negativní zásoby** pro profil umístění je nastavena na *Ne*, ale systém stále umožňuje negativní zásoby k dispozici.

## <a name="example-scenario"></a>Příklad

U vládou regulovaných transakcí musí být systém schopen zaznamenávat negativní zásoby, aby zaúčtoval ztráty. Chcete, aby položka mohla zobrazit negativní zásoby, ale pouze na určených místech, jako jsou nádrže. Pokud však skupina modelů položek umožňuje negativní zásoby, zjistíte, že nezáleží na tom, zda je umístění nastaveno tak, aby umožňovalo negativní zásoby. Pokud je položka nastavena tak, že nejsou povoleny negativní zásoby, nezáleží na tom, jak je nastaven profil polohy.

## <a name="resolution"></a>Rozlišení

Nastavení **Povolit negativní zásoby** z profilu umístění platí pouze pro procesy ve skladu, jako je vychystávání. Skupiny modelů položek, které jsou nastaveny tak, aby umožňovaly negativní zásoby, však ovlivňují všechny procesy z modulů správy zásob a správy skladu a profil umístění toto nastavení nepřepíše.

Můžete určit, zda je ve skladu povoleno provádět negativní zásoby. Nastavte skupiny modelů položek tak, aby nepovolovaly negativní fyzické zásoby, a nastavte pouze příslušný sklad, aby byly povoleny negativní zásoby.
