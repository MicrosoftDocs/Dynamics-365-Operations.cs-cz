---
title: Přihlášení zaměstnance k plánu fixní kompenzace
description: Manažer kompenzací a zaměstnaneckých výhod může přiřadit zaměstnance k plánům fixní kompenzace a spravovat tak jejich základní mzdy.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompFixedEmpl, HRMCompFixedEmplActionDialog, HcmPositionLookup, HRMCompRefPointLookup, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d611f2631a59fbe1e131e82ca9937a5adaaf2ebd
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688734"
---
# <a name="enroll-an-employee-in-a-fixed-compensation-plan"></a>Přihlášení zaměstnance k plánu fixní kompenzace


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Manažer kompenzací a zaměstnaneckých výhod může přiřadit zaměstnance k plánům fixní kompenzace a spravovat tak jejich základní mzdy. Tento postup předpokládá, že fixní plán byl vytvořen a je aktivní, a že byla nastavena pravidla způsobilosti pro daný plán. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Postup zahájíte tak, že přejděte na **Lidské zdroje** > **Pracovníci** > **Zaměstnanci** > **Kompenzace** > **Fixní plán**.

1. Klepněte na možnost **Nový**.
2. V poli **Akce** vyberte u možnosti Akce fixní kompenzace typ **Zařadit/znovu zařadit** a popište změnu v kompenzacích zaměstnance.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. V poli **Pozice** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Klikněte na odkaz na vybraném řádku v seznamu.
    * Zobrazená úroveň pochází z pole **Úroveň** na záložce **Kompenzace** z **úlohy**, která je přiřazena k **Pracovní pozici**. Úroveň musí být nastavena na stav Úloha předtím, než ji bude možné přiřadit zaměstnanci.  
6. V poli **Plán** vyberte plán fixní kompenzace pro zaměstnance. Vyhledávání **plánu** je filtrováno a zobrazí pouze plány, pro které je zaměstnanec způsobilý podle **pravidel způsobilosti**.
7. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Výchozí nastavení pro **Datum zahájení platnosti** a **Datum konce platnosti** vychází z počátečního a koncového data pro přiřazení pozice pracovníka. Tato data lze změnit podle potřeby.  
    * Je-li Plán fixní kompenzace plánem kroku, vyberte krok obsahující správné mzdové sazby pro zaměstnance. Je-li Plán fixní kompenzace plánem stupně nebo pásma, zadejte mzdovou sazbu pro zaměstnance. Mzdová sazba bude ověřena podle nastavení tolerance pro plán a minimálních a maximálních referenčních bodů pro úroveň kompenzace pozice.  
8. Klikněte na tlačítko **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
