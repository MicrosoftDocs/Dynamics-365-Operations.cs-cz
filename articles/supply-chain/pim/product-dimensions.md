---
title: Dimenze produktu
description: Existuje pět dimenzí produktu – barva, konfigurace, velikost, styl a verze. Kombinujte dimenze produktu ve skupinách dimenzí a přiřazujte skupiny dimenzí k základním produktům. Kombinace dimenzí produktu určuje způsob definování variant produktu.
author: t-benebo
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle, EcoResVersionNameLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 680d5ed929a396bfb2d3c7f05351ab6c93d29256c825c618cb166aac444aa5d6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726890"
---
# <a name="product-dimensions"></a>Dimenze produktu

[!include [banner](../includes/banner.md)]

Existuje pět dimenzí produktu: barva, konfigurace, velikost, styl a verze. Kombinujte dimenze produktu ve skupinách dimenzí a přiřazujte skupiny dimenzí k základním produktům. Kombinace dimenzí produktu určuje způsob definování variant produktu.

Dimenze produktu jsou vlastnosti, které slouží k identifikaci varianty produktu. Kombinace dimenzí produktu slouží k definování variant produktu. Chcete-li vytvořit variantu produktu, je nutné definovat alespoň jednu dimenzi produktu pro základní produkt.

## <a name="product-variants"></a>Varianty produktu

Varianty produktu jsou označovány také jako položky. Položka je hmotný produkt, který není stejný jako služba. Je také možné definovat základní produkt s typem Servis. Pomocí typu Služba můžete specifikovat varianty produktu, které obsahují služby. Můžete například určit základní produkt pro konzultační práci a varianty produktu pro práci, kterou zajišťují vyšší konzultanti a nižší konzultanti.

## <a name="product-dimensions"></a>Dimenze produktu

Varianty produktu lze generovat na základě hodnot dimenzí produktu.

Hodnoty dimenzí produktu pro rozměry, barvy a styl dimenzí lze vytvořit na následujících místech:

- Stránka **Velikosti** (**Řízení informací o produktech \> Nastavit \> Skupiny dimenzí a variant \> Velikosti**)
- Stránka **Barvy** (**Řízení informací o produktech \> Nastavit \> Skupiny dimenzí a variant \> Barvy**)
- Stránka **Styly** (**Řízení informací o produktech \> Nastavit \> Skupiny dimenzí a variant \> Styly**)

Hodnoty dimenze produktu pro konfigurační dimenze jsou obvykle tvořeny pomocí konfigurátoru produktu nebo konfigurátoru založeného na dimenzích. 

Verze produktu se obvykle vytvářejí pro konkrétní verze, protože se produkt vyvíjí během jeho životního cyklu. Verze produktu jsou podrobně popsány dále v tomto tématu.

Dimenze produktu se také vytvářejí a udržují na stránce **Dimenze produktu**, která je přístupná z následujících umístění:

- Přejděte do nabídky **Řízení informací o produktech \> Produkty \> Základní produkty**. V podokně akcí vyberte **Dimenze produktu**.
- Klikněte na **Řízení informací o produktech \> Produkty \> Všechny produkty a základní produkty**. Vyberte základní produkt. V podokně akcí vyberte **Dimenze produktu**.
- Klikněte na možnosti **Řízení informací o produktech \> Uvolněné produkty**. Vyberte základní produkt. V podokně akcí na kartě **Produkt** ve skupině **Základní produkt** zvolte **Domenze produktu**.

Počet variant, které je možné vytvořit pro položku, je omezen počet možných kombinací dimenzí produktu.

> [!TIP]
> Používáte-li na produkt, například na řádku objednávky, vyberete dimenze produktu pro identifikování varianty produktu, se kterou chcete pracovat.

## <a name="example"></a>Příklad

Společnost prodává džíny. Tato položka, *džíny*, používá pro dimenzi produktu barvy a velikosti. Džíny se prodávají ve třech různých barvách a šesti různých velikostech. Barvy jsou modrá, černá a hnědá. Velikosti jsou XS, S, M, L, XL a XXL. Ne všechny velikosti jsou k dispozici ve všech třech barvách. Pokud by byly všechny kombinace dostupné, výsledkem by bylo 18 různých druhů džín. V tomto příkladu se ale vyrábí pouze těchto devět kombinací variant produktu.

| Barva | Velikost |
|-------|------|
| Modrá  | XS   |
| Modrá  | S    |
| Modrá  | mil.    |
| Černá | mil.    |
| Černá | L    |
| Černá | XL   |
| Červenohnědá | L    |
| Červenohnědá | XL   |
| Červenohnědá | XXL  |

## <a name="the-version-product-dimension"></a>Verze dimenze produktu

Verze je dimenze produktu, která vám má pomoci udržovat a sledovat více verzí produktu v dodavatelském řetězci. Sledování verzí je zásadní pro úspěch výrobců, kteří působí ve světě neustále se snižujících životních cyklů výrobků, zvýšených požadavků na kvalitu a spolehlivost a většího zaměření na bezpečnost výrobků.

Jako standardní rozměr produktu se verze bude chovat podobně jako stávající rozměry produktu (velikost, styl, barva a konfigurace). Proto ji můžete použít pro jiné účely než sledování verzí produktu.

### <a name="turn-on-the-version-dimension"></a><a name="enable-version-dim"></a>Zapnout dimenzi verze

#### <a name="before-you-turn-on-the-version-dimension"></a>Než zapnete dimenzi verze

Když zapnete dimenzi verze, některé funkce se mohou rozbít nebo přestat fungovat podle očekávání, pokud jste nainstalovali jiná řešení, která přidávají přizpůsobení k dimenzím inventáře. Aby byla domenze verze plně funkční, možná budete muset tato řešení aktualizovat tak, aby zahrnovala dimenzi verze do svých odkazů na dimenze inventáře.

Při testování kompatibility řešení s dimenzí verze hledejte následující prvky:

1. **Funkčnost:** Nejdůležitější je, že všechny úpravy, které zahrnují dimenze inventáře, musí být posouzeny, aby bylo zajištěno, že fungují ve spojení s dimenzí verze.
1. **Odkazy na dimenze inventáře:** Dávejte pozor na odkazy na dimenze zásob (tj. Na místa, kde jsou dimenze explicitně odkazovány). Odkazy na `InventDimId` by měly fungovat mimo pole, ale dávejte pozor na odkazy na styl nebo barvu. Nezapomeňte například zkontrolovat následující prvky:

    - Volání API v rozšířených třídách
    - Všechny odkazy na konkrétní dimenze zásob v kódu rozšíření (Tento kód musí být plovoucí dohromady s dimenzemi verze, styl, barva a velikost.)

1. **Odkazy na zastaralé volání API:** Při zavedení dimenze verze se společnost Microsoft pokusila učinit co nejmenší počet API zastaralými. Několik API, které již byly zastaralé, zobrazí varování, když zapnete **Dimenze produktu - verze** konfigurační klíč. Volání na tato API musí být ve vašich rozšířených řešeních opravena, než zapnete dimenzi verze ve výrobním systému. Zde jsou zastaralá API specifická pro konkrétní verzi:

    - RetailTransactionServiceInventory::getProductRecordId
    - EcoResProductNumberIdentifiedProductVariantEntity::find
    - EGAISAlcoholProduction_RU::findByItemDim
    - PCVariantConfiguration::findByProductMasterAndDimensions

1. **Mapy:** Pokud některé mapy používají dimenze zásob, musí být odpovídající mapování relací k těmto mapám aktualizováno tak, aby obsahovaly dimenzi verze. V rozšířeném modelu nebo rozšíření tabulky hledejte tabulky, kde pole obsahují rozměry inventáře.
1. Funkce **Microsoft Dynamics 365 Commerce:** Po zapnutí se dimenze verze zobrazí v celém kódu pro obchod v Dynamics 365 Supply Chain Management. Dimenze verze však zatím není podporována databází kanálu Commerce ani aplikacích POS nebo elektronického obchodování. Tyto aplikace specifické pro obchod nebudou podporovat uživatele, kteří prodávají / odesílají nebo vracejí / přijímají zásoby podle dimenze verze. Funkce vyhledávání dostupnosti zásob nerozlišují zásoby podle dimenze verze v obchodních aplikacích. Toto chování se podobá současnému chování konfigurační dimenze v celém obchodu.

#### <a name="turn-on-the-version-dimension"></a>Zapnout dimenzi verze

Než můžete použít dimenzi verze, musíte ji zapnout ve svém systému. Tato úloha vyžaduje oprávnění správce.

1. Přejděte do nabídky **Správa systému \> Pracovní prostory \> Správa funkcí**.
1. Zapněte funkci s názvem *Dimenze verze produktu*. (Další informace naleznete v tématu [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Uveďte systém do [režimu údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).
1. Přejděte do nabídky **Správa systému \> Nastavení \> Konfigurace licence**.
1. Na **Konfigurační klíče** kartě, rozbalte **Obchod** a zaškrtněte políčko **Dimenze produktu - verze**.
1. Vypněte [Režim údržby](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).

### <a name="areas-where-the-version-dimension-isnt-supported"></a>Oblasti, kde dimenze verze není podporována

Následující oblasti nepodporují dimenzi verze (tyto oblasti můžete nadále používat, ale nebudete do nich moci přidávat produkty s verzí (produkty, kde se používá dimenze verze)). Například nemůžete přidat položku verzí do katalogu dodavatele. Je to proto, že přidání produktů s dimenzí verze do těchto oblastí by vedlo ke změnám způsobujícím chybu.

- Měsíční výpis nákladů objektu
- Mezipaměť výpisu objektu nákladů
- Statistiky prodeje MCR na položku
- Katalogy dodavatele
- EcoResProductDimensionGroupEntity

Kromě toho funkce vytváření objednávek a zpracování objednávek v Commerce (například pro objednávky POS, call centra a objednávky elektronického obchodu) nepodporují dimenzi verze. Neexistuje potvrzená časová osa, kdy bude do objednávek Commerce tato funkce přidána.

### <a name="functional-characteristics-of-the-version-dimension"></a>Funkční charakteristiky dimenze verze

Dimenze verze funguje jako ostatní dimenze produktu. Vzhledem ke své specifické povaze a protože má za cíl udržovat a sledovat více verzí produktu, chová se trochu jinak. Zde jsou některé rozdíly a podobnosti:

- **Neexistuje žádná skupina verzí.**

    Přestože koncept skupin existuje pro velikost, barvu a styl (skupina barev, skupina velikostí a skupina stylů), neexistuje žádný koncept skupiny verzí. Skupiny umožňují předdefinovat použitelné hodnoty, takže když například přiřadíte skupině produktů barvu, produkt může použít všechny barvy v této skupině barev. Tento koncept se nevztahuje na dimenzi verze, protože verze, které produkt získá, nejsou při vytváření produktu předdefinovány. Místo toho jsou verze vytvářeny během životního cyklu produktu, jak jsou vyžadovány. Typicky, pokud forma, fit a funkce produktu zůstanou stejné, vytvoříte novou verzi namísto nového produktu.

- **Návrhy variant produktu budou fungovat tak, jak doposud.**

    Návrhy variant produktu vytvoří návrhy pro všechny hodnoty dimenzí verze, stejně jako pro jiné dimenze. Proces vytváření a uvolňování verzí produktů je stejný jako u produktů, které používají jiné dimenze. Když vytvoříte produkt s verzemi, první verze (V1) bude vytvořena jako rozměr produktu a varianty budou uvolněny. Když se produkt mění a je potřebná nová verze, bude přidána nová hodnota verze (V2) a budou uvolněny požadované varianty. Neočekává se, že všechny verze (V1, V2 a V3) budou vytvořeny předem pro produkt.

> [!IMPORTANT]
> Pokud zapnete a použijete dimenzi verze, některá řešení, která odkazují na rozměry inventáře, přestanou fungovat podle očekávání. Chcete-li tyto problémy potvrdit a opravit, obraťte se na nezávislého dodavatele softwaru (ISV) ohledně řešení, kterých se to týká. Další informace viz [Povelte dimenzi verze](#enable-version-dim).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]