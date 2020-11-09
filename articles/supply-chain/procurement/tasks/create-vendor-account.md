---
title: Vytvoření účtu dodavatele
description: Tento postup popisuje vytvoření účtu dodavatele a přidání adresy a kontaktních informací.
author: mkirknel
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd8cd2bb7b03c0415a5c5656f0e3ffada961973e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017200"
---
# <a name="create-a-vendor-account"></a>Vytvoření účtu dodavatele

[!include [banner](../../includes/banner.md)]

Tento postup popisuje vytvoření účtu dodavatele a přidání adresy a kontaktních informací. Postup neukazuje vyplnění všech polí pro nákupní a finanční účely. Další informace o těchto polích naleznete v popisech polí. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Účty dodavatele jsou obvykle vytvářeny pracovníky zásobování nebo zaměstnanci starající se o pohledávky.


## <a name="create-a-vendor-account"></a>Vytvoření účtu dodavatele
1. Přejděte na **Navigační podokno > Moduly > Zásobování a zdroje > Dodavatelé > Všichni dodavatelé**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Účet dodavatele**.
    - Hodnota může být vyplněna automaticky. Pokud tomu tak je, můžete tento krok vynechat.  
    - Můžete vytvořit účty dodavatelů pro osobu nebo organizaci. Tato akce ovlivní dostupnost polí. V tomto příkladu vytvoříte účet dodavatele pro organizaci.   
4. V poli **Název** zadejte nebo vyberte hodnotu. Pokud je daný dodavatel již registrovanou stranou v systému, můžete použít rozevírací seznam a vybrat jej v tomto poli, přičemž nový účet dodavatele převezme adresu a kontaktní informace, které jsou již registrované.
5. V poli **Skupina** zadejte nebo vyberte hodnotu. Skupina dodavatelů se používá pro seskupení dodavatelů, kteří mají společné následující parametry: platební podmínky, období vyrovnání, skladové účty hlavní knihy včetně skupiny DPH, výchozí účty hlavní knihy, kódy filtru produktu a konfigurace prognózy dodávek.
6. Do pole **Počet zaměstnanců** zadejte číslo.
7. Zadejte hodnotu do pole **Číslo organizace**.

## <a name="add-an-address"></a>Přidání adresy
1. Rozbalte sekci **Adresy**.
2. Klikněte na tlačítko **Přidat**.
3. V poli **Účel** zadejte nebo vyberte hodnotu. Lze vybrat jeden nebo více účelů. Ty se používají k výběru správné adresy pro daný účel. Například pokud je účelem "Faktura", daná adresa bude použita při odesílání faktur.
4. Zadejte hodnotu do pole **Název nebo popis**.
5. V poli **Země/oblast** zadejte nebo vyberte hodnotu. Zadejte podrobnosti adresy. Vámi vybraná země/oblast určuje pole, která se zobrazí, a budou odpovídat formátu adresy pro danou zemi nebo oblast. 
6. Klikněte na tlačítko **OK**.

## <a name="add-contact-information"></a>Přidání kontaktních informací
1. Rozbalte oddíl **Kontaktní informace**.
2. Klikněte na tlačítko **Přidat**.
3. Zadejte hodnotu do pole **Popis**.
4. Vyberte volbu v poli **Typ**.
5. Zadejte hodnotu do pole **Kontaktní číslo/adresa**. Pole Primární můžete vybrat, je-li daná adresa primární adresou kontaktní osoby.  
6. Klikněte na možnost **Uložit**.
7. Zavřete stránku.
8. Zavřete stránku.

