---
title: Přihlášení zaměstnance k plánu variabilní kompenzace
description: Manažer kompenzací a zaměstnaneckých výhod může přihlásit zaměstnance do plánů variabilní kompenzace a vypočítat tak hotovostní a bezhotovostní odměny pro zaměstnance.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMCompVarEnrollEmpl
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2e591f471036c4b7f314155f1b56e87094ef1031
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008358"
---
# <a name="enroll-an-employee-in-a-variable-compensation-plan"></a>Přihlášení zaměstnance k plánu variabilní kompenzace

Manažer kompenzací a zaměstnaneckých výhod může přihlásit zaměstnance do plánů variabilní kompenzace a vypočítat tak hotovostní a bezhotovostní odměny pro zaměstnance. Tento postup předpokládá, že byl vytvořen plán variabilní kompenzace, ve kterém je v poli Povolit přihlášení nastavena hodnota Ano, a že byla vytvořena pravidla způsobilosti pro tento plán variabilní kompenzace. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Tento postup zahájíte tak, že přejděte na Lidské zdroje > Pracovníci > Zaměstnanci > Kompenzace > Zápis variabilního plánu

1. Klikněte na položku Nová.
2. V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
    * Vyhledávání plánu bude filtrováno a zobrazí pouze plány variabilní kompenzace, pro které je zaměstnanec způsobilý podle pravidel způsobilosti.  
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Přepněte rozšíření oddílu Obecné.
5. Zadejte datum do pole Datum platnosti.
6. Klikněte na položku Uložit.
7. Přepněte rozšíření oddílu Přepsání.
    * V případě potřeby lze nastavit datum pravidla zařazení tak, aby přepsalo datum zařazení zaměstnance v případě, že je u pravidla zařazení pro vybraný variabilní plán vybrána možnost Procento.  
    * Pokud variabilní plán je plánem využívajícím procentuální část základu, je možné pro zaměstnance přepsat procentuální odměnu. Pokud plán variabilní kompenzace je plánem využívajícím počet jednotek, je možné pro zaměstnance přepsat počet jednotek.  
    * Pokud by měla být zaměstnanci dána prostá částka představující jejich odměnu, tuto částku můžete nastavit zde.  
8. Přepněte rozšíření oddílu Organizační přepsání.
    * Je-li třeba zohlednit výkon zaměstnance, je možné přepsat výkon v ostatních odděleních nebo oddělení jiném, než které je přiřazeno pro pozici zaměstnance. Sloupec Procento musí dohromady dát číslo 100.  
