---
title: Zpracování způsobilosti k registraci
description: Tento článek vysvětluje, jak spustit proces nároku na přihlášení.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f9b1febe2690fab17586033994b10ebf260630af
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805699"
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

2.  Ve formuláři **Zpracovat výsledky** se specifikují následující pole:

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