---
title: Vytvoření rozšířených pravidel pro deníky
description: Tento postup vás provede vytvářením rozšířených pravidel pro deníky.
author: aprilolson
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f5cc41f19928fd415fb54073fd733f97a3e7aa01
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717411"
---
# <a name="create-advanced-rules-for-journals"></a>Vytvoření rozšířených pravidel pro deníky

[!include [banner](../../includes/banner.md)]

Tento postup vás provede vytvářením rozšířených pravidel pro deníky. To zahrnuje nastavení deníků, řízení a omezení zaúčtování uživatele. Tato procedura používá data ukázkové společnosti USMF.


## <a name="set-up-journal-control"></a>Nastavení kontroly deníku
1. V **navigačním podokně** přejděte na **Moduly > Hlavní kniha > Nastavení deníku > Názvy deníku**.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. V **Podokně akcí** klikněte na možnost **Kontrola deníku**.
4. Na záložce s náhledem **Které typy účtů lze zaúčtovat** klikněte **Přidat**.
5. V poli **Účty společnosti** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. Na záložce s náhledem **Které hodnoty segmentu jsou platné pro tento deník** klikněte na **Přidat**.
9. V poli **Účetní struktura** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
10. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
11. Klikněte na odkaz na vybraném řádku v seznamu.
12. V poli **Segment** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
13. Klikněte na odkaz na vybraném řádku v seznamu.
14. V poli **Od hodnoty** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
15. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
16. Klikněte na odkaz na vybraném řádku v seznamu.
17. V poli **Do hodnoty** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
18. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
19. Klikněte na odkaz na vybraném řádku v seznamu.

## <a name="set-up-posting-restrictions"></a>Nastavení omezení zaúčtování
1. Zavřete stránku.
2. Klikněte na **Omezení účtování**.
3. V poli **Jak chcete nastavit omezení zaúčtování** vyberte možnost Podle skupin uživatelů.
4. Ve stromu zkontrolujte „skupinu, pro kterou chcete povolit zaúčtování pro tento název deníku“.
5. Klikněte na tlačítko **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
