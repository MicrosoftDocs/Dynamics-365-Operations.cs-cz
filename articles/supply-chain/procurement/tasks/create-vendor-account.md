---
title: Vytvoření účtu dodavatele
description: Tento postup popisuje vytvoření účtu dodavatele a přidání adresy a kontaktních informací.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22c7a1a2b7468f00aa25a67a2c5f62b088e2fe7c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "360134"
---
# <a name="create-a-vendor-account"></a>Vytvoření účtu dodavatele

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje vytvoření účtu dodavatele a přidání adresy a kontaktních informací. Postup neukazuje vyplnění všech polí pro nákupní a finanční účely. Další informace o těchto polích naleznete v popisech polí. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Účty dodavatele jsou obvykle vytvářeny pracovníky zásobování nebo zaměstnanci starající se o pohledávky.


## <a name="create-a-vendor-account"></a>Vytvoření účtu dodavatele
1. Přejděte na Zásobování a zdroje > Dodavatelé > Všichni dodavatelé.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Účet dodavatele.
    * Hodnota může být vyplněna automaticky. Pokud tomu tak je, můžete tento krok vynechat.  
    * Můžete vytvořit účty dodavatelů pro osobu nebo organizaci. Tato akce ovlivní dostupnost polí. V tomto příkladu vytvoříte účet dodavatele pro organizaci.   
4. V poli Název zadejte nebo vyberte hodnotu.
    * Pokud je daný dodavatel již registrovanou stranou v systému, můžete použít rozevírací seznam a vybrat jej v tomto poli, přičemž nový účet dodavatele převezme adresu a kontaktní informace, které jsou již registrované.  
5. V poli Skupina zadejte nebo vyberte hodnotu.
    * Skupina dodavatelů se používá pro seskupení dodavatelů, kteří mají společné následující parametry: platební podmínky, období vyrovnání, skladové účty hlavní knihy včetně skupiny DPH, výchozí účty hlavní knihy, kódy filtru produktu a konfigurace prognózy dodávek.  
6. Do pole Počet zaměstnanců zadejte číslo.
7. Zadejte hodnotu do pole Číslo organizace.

## <a name="add-an-address"></a>Přidání adresy
1. Rozbalte sekci Adresy.
2. Klepněte na možnost Přidat.
3. V poli Účel zadejte nebo vyberte hodnotu.
    * Lze vybrat jeden nebo více účelů. Ty se používají k výběru správné adresy pro daný účel. Například pokud je účelem "Faktura", daná adresa bude použita při odesílání faktur.  
4. Zadejte hodnotu do pole Název nebo popis.
5. V poli Země/oblast zadejte nebo vyberte hodnotu.
    * Zadejte podrobnosti adresy. Vámi vybraná země/oblast určuje pole, která se zobrazí, a budou odpovídat formátu adresy pro danou zemi nebo oblast.   
6. Klikněte na tlačítko OK.

## <a name="add-contact-information"></a>Přidání kontaktních informací
1. Klepněte na možnost Přidat.
2. Zadejte nějakou hodnotu do pole Popis.
3. Vyberte volbu v poli Typ.
4. Zadejte hodnotu do pole Kontaktní číslo/adresa.
    * Pole Primární můžete vybrat, je-li daná adresa primární adresou kontaktní osoby.  
5. Klikněte na položku Uložit.
6. Zavřete stránku.
7. Zavřete stránku.

