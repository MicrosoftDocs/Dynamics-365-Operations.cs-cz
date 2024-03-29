---
title: Zpracování způsobilosti k registraci
description: Tento článek vysvětluje, jak spustit proces nároku na přihlášení.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bd05585f691a4c6aa55a7aec7ceaaf0273f0abcb
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/23/2022
ms.locfileid: "9323474"
---
# <a name="process-enrollment-eligibility"></a>Zpracování způsobilosti k registraci

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek vysvětluje, jak spustit proces nároku na přihlášení.

1. V pracovním prostoru **Správa výhod** vyberte v části **Zpracování** možnost **Zpracování nároku na registraci**.

2. V dialogovém okně **Spustit proces nároku na registraci zaměstnanecké výhody** zadejte hodnoty pro následující pole:

   | Pole | Popis |
   | --- | --- |
   | **Období registrace** | Období pro přihlášení pro zpracování nároku na zaměstnanecké výhody. |
   | **Právnická osoba** | Právnická osoba pro zpracování nároku na registraci. |
   | **Pracovní podproces** | Pracovník pro zpracování nároku na registraci. Pokud toto pole ponecháte prázdné, bude nárok na registraci zpracován pro všechny pracovníky. |
   | **Plán zaměstnaneckých výhod** | Plán zaměstnaneckých výhod pro zpracování nároku na registraci.

3. Chcete-li spustit proces na pozadí, vyberte možnost **Spustit na pozadí** a proveďte následující úkony:

   1. Zadejte informace pro proces.

   2. Chcete-li nastavit opakovanou úlohu, vyberte možnost **opakování**, zadejte informace o opakování a vyberte **OK**.

   3. Chcete-li nastavit výstrahu úlohy,vyberte **výstrahy**, vyberte výstrahy, které chcete přijmout, a pak vyberte **OK**.

   4. Vyberte **OK**. Proces bude spuštěn s nastavenými parametry.

4. Vyberte **OK**.

## <a name="view-process-results"></a>Zobrazit výsledky procesu

Tento článek vysvětluje, jak zobrazit výsledky procesu nároku.

1.  V pracovním prostoru **Správa výhod** vyberte v části **Zpracování** možnost **Zpracovat výsledky**.

2.  Ve stránce **Zpracovat výsledky** jsou zadána následující pole:

   | Pole | popis |
   | --- | --- |
   | **ID procesu** | Jedinečné ID pro kombinaci pracovníka, právnické osoby a běhu procesu. |
   | **Typ procesu** | Tím se identifikuje proces, který byl spuštěn. Například: Přihlášení. |
   | **Časový údaj** | Čas, kdy byl spuštěn proces nároku. |
   | **Právnická osoba** | Právnická osoba určená v průběhu procesu zápisu. |
   | **Pracovní podproces** | Pracovník, který byl zpracován. |
   | **Plán | Plán zaměstnaneckých výhod, pro který byl proveden pokus o zápis. |
   | **Pravidlo způsobilosti** | Pravidlo způsobilosti, které bylo zpracováno. Pokud došlo k chybě před spuštěním nároku na způsobilost, bude toto pole prázdné. Například: Pokud pro pracovníka nebyla definována kompenzace, proces nároku nebude spuštěn a toto pole zůstane prázdné. |
   | **Výsledný stav** | To bude způsobilé nebo nezpůsobilé. Pokud pracovník nesplní požadované informace, jako je například četnost plateb nebo fixní kompenzace, nebo pokud v plánu zaměstnaneckých výhod chybí informace, které brání registraci zaměstnanců, nebude mít výsledný stav nárok. |
   | **Výsledná zpráva** | Označuje, proč pracovník nemá nárok na plán zaměstnaneckých výhod nebo který předává pravidlo způsobilosti. |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
