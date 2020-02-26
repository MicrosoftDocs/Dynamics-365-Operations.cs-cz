---
title: Modul pokladny
description: Tohle téma popisuje, jak na stránku přidat modul pokladny a jak nastavit požadované vlastnosti.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3805c0faabc8afc3decffb924b7f25332ff1ab16
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025383"
---
# <a name="checkout-module"></a>Modul pokladny


[!include [banner](includes/banner.md)]

Tohle téma popisuje, jak na stránku přidat modul pokladny a jak nastavit požadované vlastnosti.

## <a name="overview"></a>Přehled

Modul poklady je speciální kontejner, který je hostitelem všech modulů, které jsou nutné k vytvoření objednávky. Modul poklady představuje podrobný tok, který zákazník používá k zadání všech relevantních informací za účelem provedení nákupu. Zachycuje doručovací adresu, způsob přepravy a informace o fakturaci. Poskytuje také souhrn objednávky a další informace, které souvisejí s objednávkou odběratele.

Modul pokladny vykresluje data na základě ID košíku. ID košíku je uloženo jako soubor cookie prohlížeče. ID košíku je nutné k vykreslení informací v modulu pokladny, jako jsou například položky v objednávce, celková částka a slevy.

## <a name="checkout-module-properties"></a>Vlastnosti modulu pokladny

V modulu pokladny se zobrazí souhrn objednávek a funkce pro zadání objednávky. Chcete-li shromáždit všechny informace o odběrateli, které jsou požadovány před tím, než může být objednávka vystavena, je nutné přidat další moduly do modulu pokladny. Maloobchodní prodejci proto mají flexibilitu přidávat vlastní moduly do toku pokladny nebo vyloučit moduly na základě jejich požadavků.

### <a name="modules-that-can-be-used-in-the-checkout-module"></a>Moduly, které lze použít v modulu pokladny

- **Dodací adresa** – Tento modul umožňuje zákazníkovi přidat nebo vybrat dodací adresu objednávky. Je-li zákazník přihlášen, zobrazí se všechny adresy, které byly pro daného zákazníka dříve uloženy. Zákazník pak může z těchto adres vybírat. Zákazník může také přidat novou adresu. Dodací adresa se použije pro všechny položky v objednávce, které vyžadují dodání. Nelze ji upravit pro jednotlivé položky řádku. Formáty dodacích adres se definují pro každou zemi nebo oblast a pravidla specifická pro danou zemi nebo oblast jsou vynucena tímto modulem. Přestože tento modul neposkytuje ověřování adres, ověření adresy lze implementovat prostřednictvím vlastního nastavení. Pokud objednávka obsahuje pouze položky, které budou vydány v obchodě, bude tento modul automaticky skrytý.
- **Možnosti dodání** – Tento modul umožňuje zákazníkovi vybrat možnost dodání pro objednávku. Možnosti dodání jsou založeny na dodací adrese. Pokud se změní dodací adresa, je nutné znovu načíst možnosti dodání. Pokud objednávka obsahuje pouze položky, které budou vydány v obchodě, bude tento modul automaticky skrytý.
- **Kontejner sekce pokladny** – Tento modul je kontejner, do kterého můžete vložit více modulů a vytvořit sekci v rámci toku pokladny. Všechny moduly související s platbou v tomto kontejneru můžete například vložit do jedné sekce. Tento modul má vliv pouze na rozložení toku.
- **Dárkový poukaz** – Tento modul umožňuje zákazníkovi zaplatit za objednávku pomocí dárkového poukazu. Podporuje pouze dárkové poukazy Microsoft Dynamics 365 Commerce. Na objednávku lze použít jeden nebo více dárkových poukazů. Pokud zůstatek dárkového poukazu nepokrývá částku v nákupním košíku, může být dárkový poukaz zkombinován s jiným způsobem platby. Dárkové poukazy lze uplatnit pouze v případě, že je zákazník přihlášen.
- **Věrnostní body** – Tento modul umožňuje odběrateli zaplatit za objednávku pomocí věrnostních bodů. Poskytuje souhrn dostupných bodů a bodů s končící platností a umožňuje zákazníkovi vybrat počet bodů, které chce uplatnit. Pokud zákazník není přihlášen nebo není věrnostní člen, nebo pokud je celková částka nákupního košíku 0 (nula), bude tento modul automaticky skryt.
- **Platba** – Tento modul umožňuje zákazníkovi zaplatit za objednávku pomocí kreditní karty. Pokud je celková částka nákupního košíku pokryta věrnostními body nebo dárkovým poukazem, nebo je 0 (nula), bude tento modul automaticky skryt. Integraci kreditiní karty pro tento modul zajišťuje konektor platby Adyen. Další informace o způsobu použití tohoto konektoru naleznete v tématu [Konektor platby Dynamics 365 pro Adyen](dev-itpro/adyen-connector.md).
- **Fakturační adresa** – Tento modul umožňuje zákazníkovi zadat fakturační informace. Tyto informace jsou spolu s informacemi o kreditní kartě zpracovány konektorem platby Adyen. Tento modul zahrnuje možnost, která zákazníkům umožňuje použít fakturační adresu jako dodací adresu.
- **Kontaktní informace** – Tento modul umožňuje zákazníkovi přidat nebo změnit kontaktní informace (e-mailovou adresu) na objednávce.
- **Textový blok** – Tento modul zahrnuje veškerá zasílání zpráv, která jsou řízena systémem správy obsahu (CMS). Může například obsahovat zprávu ve znění „V případě problémů s objednávkou volejte 1-800-Fabrikam“. 

## <a name="commerce-scale-unit-interaction"></a>Interakce Commerce Scale Unit

Většina informací o pokladně, například dodací adresa a způsob dodání, je uložena v nákupním košíku a zpracována jako součást objednávky. Jedinou výjimkou jsou informace o kreditní kartě. Tyto informace jsou zpracovávány přímo pomocí konektoru platby Adyen. Platba je autorizována, ale není účtována.

## <a name="add-a-checkout-module-to-a-new-page-and-set-the-required-properties"></a>Na novou stránku přidejte modul pokladny a nastavte požadované vlastnosti.

Chcete-li přidat modul pokladny na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Předjěte na **Fragment \> Nový fragment** a pojmenujte nový fragment jako **Fragment pokladny**.
1. Přidejte do fragmentu modul pokladny.
1. Přidejte do modulu pokladny nadpis.
1. Přidat dodací adresu, možností dodání, kontejneru sekce pokladny a kontaktních informací. 
1. V modulu kontejneru sekce pokladny přidejte moduly dárkového poukazu, věrnostních bodů a platby. Tímto způsobem zajistíte, že se všechny způsoby platby budou v sekci zobrazovat společně.
1. Uložení a náhled fragmentu. Některé moduly, které nemají kontext nákupního košíku, nemusí být v náhledu vykresleny.
1. Dokončete úpravy fragmentu a publikujte jej.
1. Vytvořte šablonu která používá nový fragment pokladny.
1. Vytvořte stránku pokladny, která používá novou šablonu.

## <a name="additional-resources"></a>Další zdroje

[Přehled startovací sady](starter-kit-overview.md)

[Modul kontejneru](add-container-module.md)

[Modul buy boxu](add-buy-box.md)

[Modul košíku](add-cart-module.md)

[Modul potvrzení objednávky](order-confirmation-module.md)

[Modul záhlaví](author-header-module.md)

[Modul zápatí](author-footer-module.md)
