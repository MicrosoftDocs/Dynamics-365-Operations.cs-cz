---
title: Přihlášení zaměstnance k plánu fixní kompenzace
description: Manažer kompenzací a zaměstnaneckých výhod může přiřadit zaměstnance k plánům fixní kompenzace a spravovat tak jejich základní mzdy.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc8373a4a39a1a212ab445b2b300fbddfe0e4a39
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111791"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>Přihlášení zaměstnance k plánu fixní kompenzace

Manažer kompenzací a zaměstnaneckých výhod může přiřadit zaměstnance k plánům fixní kompenzace a spravovat tak jejich základní mzdy. Tento postup předpokládá, že fixní plán byl vytvořen a je aktivní, a že byla nastavena pravidla způsobilosti pro daný plán. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Postup zahájíte tak, že přejděte na Lidské zdroje > Pracovníci > Zaměstnanci > Kompenzace > Fixní plán

1. Klikněte na položku Nová.
2. V poli Akce vyberte u možnosti Akce fixní kompenzace typ Zařadit nebo znovu zařadit a popište změnu v kompenzacích zaměstnance.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. V poli Pozice kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Klikněte na odkaz na vybraném řádku v seznamu.
    * Uvedená úroveň pochází z úrovně kompenzace pro úlohu na dané pozici. Úroveň musí být nastavena na stav Úloha předtím, než ji bude možné přiřadit zaměstnanci.  
6. V poli Plán vyberte plán fixní kompenzace pro zaměstnance. Vyhledávání plánu je filtrováno a zobrazí pouze plány, pro které je zaměstnanec způsobilý podle pravidel způsobilosti.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Výchozí nastavení pro Datum zahájení platnosti a Datum konce platnosti vychází z počátečního a koncového data pro přiřazení pozice pracovníka. Tato data lze změnit podle potřeby.  
    * Je-li Plán fixní kompenzace plánem kroku, vyberte krok obsahující správné mzdové sazby pro zaměstnance. Je-li Plán fixní kompenzace plánem stupně nebo pásma, zadejte mzdovou sazbu pro zaměstnance. Mzdová sazba bude ověřena podle nastavení tolerance pro plán a minimálních a maximálních referenčních bodů pro úroveň kompenzace pozice.  
8. Klikněte na tlačítko OK.



[!INCLUDE[footer-include](../includes/footer-banner.md)]