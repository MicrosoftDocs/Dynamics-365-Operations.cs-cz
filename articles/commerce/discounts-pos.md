---
title: Zobrazit slevy v POS
description: Toto téma vysvětluje, jak Microsoft Dynamics 365 Commerce pomáhá prodejcům získat informace o promoakcích a způsobu jejich použití pro křížové a návazné pohyby.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-Commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail, Commerce
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: Application update 10.0.10
ms.openlocfilehash: 54201de6b242f8100c19a78468476a6308b1b18a
ms.sourcegitcommit: 5554b3abb4365666992efad692ae28e943faebd4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/11/2020
ms.locfileid: "3116549"
---
# <a name="show-discounts-in-pos"></a>Zobrazit slevy v POS

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Promoakce hrají důležitou roli při motivaci zákazníků, kteří provádějí nákupní rozhodnutí. Svátky mohou například zajistit nejvyšší počet prodejů maloobchodníkům, protože celý maloobchodní trh je zaplaven promoakcemi a slevami. Pokud členové obchodu informují informace o dostupných promoakcích a rozumíte jim, mohou tyto promoakce snadno využít k propagaci křížových a návazných položek. Toto téma vysvětluje, jak Microsoft Dynamics 365 Commerce pomáhá prodejcům získat informace o promoakcích a způsobu jejich použití pro křížové a návazné pohyby.

## <a name="learn-about-store-discounts"></a>Informace o skladovacích slevách

Commerce obsahuje operaci nazvanou "Zobrazit všechny slevy". Tato operace zobrazí všechny slevy, které jsou aktuálně spuštěny v obchodě. Operaci "Zobrazit všechny slevy" lze mapovat na tlačítko na pokladním místě (POS) a toto tlačítko lze přidat na stránku **Vítejte** nebo na stránku **Transakce**. Následující ilustrace znázorňuje příklad otevřené stránky **Všechny slevy**.

![Stránka Všechny slevy](./media/View_all_discounts.png "Stránka Všechny slevy")

Chcete-li zobrazit slevy, systém vyhledá všechny slevy, které odpovídají jedné nebo více z následujících podmínek:

- Cenová skupina slevy se shoduje s cenovou skupinou obchodu.
- Cenová skupina slevy je mapována na afilaci nebo věrnostní program.
- Cenová skupina slevy je mapována na katalog přidružený k obchodu.

Na stránce **Všechny slevy** jsou zobrazeny pouze některé slevy na základě kupónu, protože maloobchodní prodejci obvykle vytvářejí tisíce kupónů a odpovídajících slev pro jedinečné zákazníky a tato stránka není určena k zobrazení slev specifických pro zákazníka. Slevy založené na kupónech jsou zobrazeny pouze v případě, že je v každém záhlaví kupónu zaškrtnuto políčko **Použít bez kódu kupónu**. V takovém případě mohou pokladníci použít kupón bez nutnosti zadávat nebo kontrolovat kód kupónu nebo čárový kód.

Pokud je možnost **Použít bez kódu kupónu** zapnuta, budou k dispozici různé scénáře. Například pokladníci mohou zákazníkům dodat další slevy za účelem uklidnění zákazníka nebo z důvodu vad produktu. Tištěné kódy kupónů nebo čárové kódy nemusí být distribuovány pokladníkům. Místo toho mohou pokladníci vybrat tlačítko **Použít kupón**. Kupón se poté automaticky použije na transakci. Pokud pro záhlaví kupónu existuje více kupónů, systém automaticky vybere první aktivní kupón v transakci.

Na stránce **Všechny slevy** mohou prodejci tyto slevy vyhledávat také podle klíčových slov. Vyhledávání klíčových slov prohledá pole, která obsahují název slevy a popis slevy. Prodejci mohou také filtrovat slevy na základě toho, zda sleva vyžaduje kód kupónu.

## <a name="cross-sell-and-upsell-by-using-discounts"></a>Křížový prodej a návazný prodej pomocí slev

Víceřádkové slevy, jako například množstevní slevy, kombinační slevy a mezní slevy, jsou skvělým způsobem, jak motivovat zákazníky při nákupu více produktů za účelem získání větších slev. Proto také pomohou zvýšit výnosy z košíku odběratele a maloobchodního prodeje. Tyto slevy lze zveřejnit na webech e-commerce, na sociálních médiích a na bannerech v obchodě.

I když jsou však všechny tyto metody propagace použity, mohou zákazníci vymezit možnost využívat promoakce. Chcete-li pro prodejce usnadnit získání informací o promoakcích, které lze použít pro vybraný řádek, nebo dokonce na celý nákupní košík, mohou maloobchodní prodejci přidat tlačítko pro operaci "Zobrazit všechny slevy" do libovolné mřížky tlačítek v POS. Doporučujeme přidat tlačítko do mřížky tlačítek na stránce **Transakce**. V takovém případě může prodejní sdružení vybrat řádek transakce a poté vybrat tlačítko pro zobrazení všech slev, které jsou k dispozici pro vybraný řádek. Prodejci mohou také vybrat jinou kartu zobrazující slevy, které se vztahují na celou transakci.

Na stránce **Všechny slevy**, která byla zmíněna dříve, jsou zobrazeny pouze slevy, které neodpovídají žádné z použitých slev. Toto chování pomáhá zajistit, že v případě, že prodávající informuje odběratele o slevě a odběratel provede požadovanou akci (například odběratel nakoupí jednu další položku pro získání 10 procent), sleva bude uplatněna na transakci. Jak již bylo uvedeno, slevy založené na kupónech jsou zobrazeny pouze v případě, že je zapnuta možnosti **Použít bez kódu kupónu**.

V jednoduchém scénáři, kdy všechny slevy mají stejnou prioritu, je režim souběžnosti slevy **Složený** a řízení souběžnosti slev je nastaveno na **Nejlepší cenu a složit v rámci priority, nikdy neskládat mezi prioritami**, na stránce **Všechny slevy** jsou zobrazeny všechny slevy dostupné pro produkt, protože všechny slevy jsou složeny a vzájemně si nekonkurují.

Následující ilustrace znázorňují logiku, která určuje, které slevy se zobrazí ve složitějších scénářích, například v případě, kdy je režim souběžnosti **Nejlepší cena** nebo **Výlučný** a jsou použity dvě nebo více priorit. V těchto scénářích jsou zobrazené slevy dále ovlivněny na základě toho, zda je řízení souběžnosti nastaveno na **Nejlepší cena a složená v prioritě, nikdy neskládat napříč prioritami** nebo **Nejlepší cena pouze v rámci priority, vždy skládat napříč prioritou**.

Na následujícím obrázku je znázorněna logika, která se používá v případě, že je řízení souběžnosti nastaveno na **Nejlepší cena a složená v prioritě, nikdy neskládat napříč prioritami**.

![Logika pro Nejlepší cena a složená v prioritě, nikdy neskládat napříč prioritami](./media/Model_1.png "Logika pro Nejlepší cena a složená v prioritě, nikdy neskládat napříč prioritami").

Na následujícím obrázku je znázorněna logika, která se používá v případě, že je řízení souběžnosti nastaveno na **Nejlepší cena pouze v rámci priority, vždy skládat napříč prioritou**.

![Logika pro Nejlepší cena pouze v rámci priority, vždy skládat napříč prioritou](./media/Model_2.png "Logika pro Nejlepší cena pouze v rámci priority, vždy skládat napříč prioritou").