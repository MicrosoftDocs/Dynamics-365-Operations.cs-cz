---
title: Přihlášení zaměstnance k plánu variabilní kompenzace
description: Manažer kompenzací a zaměstnaneckých výhod může přihlásit zaměstnance do plánů variabilní kompenzace a vypočítat tak hotovostní a bezhotovostní odměny pro zaměstnance.
author: twheeloc
ms.date: 08/25/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67b3cd95276b9e59e794583fa51ddbcec4c43b1e
ms.sourcegitcommit: a8ac6d9b63eb67d14dd17a086ef4f1eccd7f9fc1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/27/2021
ms.locfileid: "7431307"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a>Přihlášení zaměstnance k plánu variabilní kompenzace

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Manažer kompenzací a zaměstnaneckých výhod může přihlásit zaměstnance do plánů variabilní kompenzace a vypočítat tak hotovostní a bezhotovostní odměny pro zaměstnance. Tento postup předpokládá, že byl vytvořen plán variabilní kompenzace, ve kterém je v poli **Povolit přihlášení** nastavena hodnota Ano, a že byla vytvořena pravidla způsobilosti pro tento plán variabilní kompenzace. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup zahájíte tak, že přejděte na **Lidské zdroje** > **Pracovníci** > **Zaměstnanci** > **Kompenzace** > **Zápis variabilního plánu**.

1. Klepněte na možnost **Nový**.
2. V poli **Plán** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Vyhledávání plánu bude filtrováno a zobrazí pouze plány variabilní kompenzace, pro které je zaměstnanec způsobilý podle pravidel způsobilosti.  
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Přepněte rozšíření oddílu Obecné.
5. Zadejte datum do pole **Datum platnosti**.
6. Klikněte na tlačítko **Uložit**.
7. Přepněte rozšíření oddílu **Přepsání**.
    * V případě potřeby lze nastavit datum pravidla zařazení tak, aby přepsalo datum zařazení zaměstnance v případě, že je u pravidla zařazení pro vybraný variabilní plán vybrána možnost Procento.  
    * Pokud variabilní plán je plánem využívajícím procentuální část základu, je možné pro zaměstnance přepsat procentuální odměnu. Pokud plán variabilní kompenzace je plánem využívajícím počet jednotek, je možné pro zaměstnance přepsat počet jednotek.  
    * Pokud by měla být zaměstnanci dána prostá částka představující jejich odměnu, tuto částku můžete nastavit zde.  
8. Přepněte rozšíření oddílu **Organizační přepsání**.
    * Je-li třeba zohlednit výkon zaměstnance, je možné přepsat výkon v ostatních odděleních nebo oddělení jiném, než které je přiřazeno pro pozici zaměstnance. Sloupec **Procento** musí dohromady dát číslo 100.  



[!INCLUDE[footer-include](../includes/footer-banner.md)]
