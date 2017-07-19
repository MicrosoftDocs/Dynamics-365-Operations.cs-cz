---
title: "Přehled informací o produktech"
description: "Toto téma poskytuje informace o správě informací o produktu. Řízení informací o produktech funguje s definicí sdíleného produktu, kategorizací a identifikátory napříč všemi právnickými osobami a také s určitými konfiguracemi produktů pro obchodní procesy."
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductListPage, EcoResProductVariantMaintainWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: cvocph
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: db8a9666518b58b6b32bb4a14933095dd9416aa0
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="product-information-overview"></a>Přehled informací o produktech

[!include[banner](../includes/banner.md)]

[!include[retail name](../includes/retail-name.md)]

Toto téma poskytuje informace o správě informací o produktu. Řízení informací o produktech funguje s definicí sdíleného produktu, kategorizací a identifikátory napříč všemi právnickými osobami a také s určitými konfiguracemi produktů pro obchodní procesy. 

Informace o produktu tvoří základní prvky dodávek dodavatelsko-odběratelského řetězce a maloobchodních aplikací pro všechna odvětví. Vztahuje se k procesům a technologiím zaměřeným na centrální správu informací o produktech (například v rámci dodavatelských řetězců). Je důležité, aby byly použity definice sdíleného produktu, dokumentaci, atributy a identifikátory. V různých modulech podnikového řešení jsou požadovány informace o produktu a konfigurace potřebné pro účely správy obchodních procesů, které souvisejí s konkrétními produkty, skupinami produktů nebo kategoriemi produktu.

## <a name="product-definition"></a>Definice produktu

Produkt je definován především číslem, názvem a popisem. Jsou však požadována také další data za účelem popisu produktu nebo služby:

- Typ produktu: Položka nebo služba
- Podtyp produktu: různé produkty nebo hlavní produkty
- Definice modelu varianty produktu:

     - Dimenze produktu a skupiny dimenzí
     - Názvosloví produktu
     - Modely konfigurace produktu

- Přidružení jedné nebo více kategorií produktu
- Definice atributů produktů a kategorií
- Obrázky produktu
- Přílohy
- Jednotky měření a související převody
- Překlady všech názvů a popisů

## <a name="distribution-export-and-import-of-product-data"></a>Distribuce, export a import dat produktu

Definici produktu lze vytvořit v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Lze ji také importovat ze správy životního cyklu produktu (PLM), správy dat správy produktů (PDM) nebo systémů správy informací o produktu (PIM). Při použití více než jedné instance aplikace Finance and Operations se jedna instance běžně používá jako předloha dat produktu pro všechny ostatní instance. Tato metoda je podpořena velkou sadou datových entit, které umožňují export a import dat definice produktů z jedné instance na jinou.

Na podporu distribuce dat produktu do mnoha instancí umožňuje aplikace Finance and Operations použití služby Common Data Service. Definice produktů lze exportovat službu běžné dat z instance aplikace Finance and Operations do služby Common Data Service. Definice produktů lze použít k zajištění jinými obchodními aplikacemi, jako například aplikace Microsoft Dynamics 365 for Sales, s daty produktu.

Všimněte si, že v dynamických a pružných organizacích se informace o produktech mění denně. Údržba přesných a skutečných dat je tedy důležitý obchodní proces sám o sobě.

## <a name="product-masters-and-product-variants"></a>Hlavní produkty a varianty produktů

V agilním, kde se produkty musí rychle podřizovat požadavkům zákazníka, určují definice produktů sadu produktů místo jedinečných produktů. V aplikaci Microsoft Dynamics 365 for Finance and Operations jsou tyto obecné produkty známy jako *hlavní produkty*. Hlavní produkty mají definici a pravidla definující způsob popisu jedinečných produktů a jejich chování v obchodních procesech. Na základě těchto definicí mohou být generovány jedinečné produkty. Tyto jedinečné produkty se označují jako *varianty produktu*.

V aplikaci Finance and Operations je hlavní produkt přidružen ke skupině dimenzí produktu a technologii konfigurace k určení obchodních pravidel. Dimenze produktu (barva, velikost, styl a konfigurace) jsou konkrétní sada atributů, které lze použít v celé aplikaci k definování a sledování konkrétního chování souvisejících produktů. Tyto dimenze také pomáhají uživatelům vyhledat a určit produkty.

## <a name="configuration-technologies"></a>Technologie konfigurace

Můžete vybírat mezi třemi technologiemi konfigurace:

- Předdefinované varianty definují předem definované dimenze produktu. Definice variant obsahuje definici specifické platné kombinace dimenzí, jako je barva, styl a velikost. Každá kombinace vytváří různé varianty produktu.
- Konfigurace založené na dimenzích se obvykle používají ve scénářích výroby a umožňují používání dimenze konfigurace v definici kusovníků (BOM). Po výběru konkrétní konfigurace systém použije podmnožinu řádků kusovníku, které jsou platné pro danou konfiguraci plánování a výroby. Tento koncept je známý také jako *globální kusovníku*, protože se jeden sdílený kusovník používá pro všechny konfigurace produktu.
- Konfigurace založená na omezeních používá k popisu všech možných atributů a součástí, které jsou požadovány pro všechny možné varianty produktu, jeden modul konfigurace produktu. Omezení kombinací atributů lze popsat pomocí regulárních výrazů nebo omezení na základě tabulky. Modely konfigurace a konfigurátory začnou být důležitější v modulu řízení informací o produktu a používají se ve všech odvětvích.

Při plánování implementace aplikace Finance and Operations je velmi důležité zvolit správnou technologii konfigurace pro obchodní proces. Produkt nelze převést z jednoho modelu na jiný po implementaci.

## <a name="product-variant-model-definition-workspace"></a>Pracovní prostor Definice modelu varianty produktu

Pracovní prostor **Definice variant modelu produktu** poskytuje přehled hlavních produktů. Rovněž zobrazuje stav vydání hlavních produktů a souvisejících variant konkrétním právnickým osobám.

## <a name="released-products"></a>Uvolněné produkty

Produkty, které budou uvolněny pro určitou právnickou osobu, se označují jako *uvolněné produkty*. Produkty lze uvolňovat hromadně pro jednu právnickou osobu nebo mnoho právnických osob vždy po jednom. Vzhledem k tomu, že různé vlastnosti a atributy produktu mohou být přidávány podle právnických osob, pracovní prostor **Údržba uvolněného produktu** vám umožní sledovat a dokončit naposledy uvolněné produkty v každé právnické osobě nebo v dílčích organizacích právnické osoby.

### <a name="released-product-maintenance-workspace"></a>Pracovní prostor Údržba uvolněného produktu

Pracovní prostor **Údržba uvolněného produktu** lze konfigurovat z položky nabídky **Nakonfigurovat můj pracovní prostor**. Vyberte hierarchii kategorií a kategorii pro filtrování pracovního prostoru. Chcete-li upravit příslušná data produktu v pracovním prostoru, můžete také definovat časové limity pro **naposledy uvolněné produkty** a **zastavené uvolněné produkty** ve dnech.

Pracovní prostor sestává ze souhrnu dlaždic a dvou seznamů. Seznam **Otevřené případy** zobrazuje případy změny produktu, které mají produkty ve vybrané hierarchii kategorie produktů, které nejsou dokončeny a uzavřeny. Seznam **Naposledy uvolněné** zobrazuje produkty, které byly uvolněny v rámci časového limitu nastaveného v konfiguraci pracovního prostoru. Pro každou položku v seznamu se spustí ověření a zobrazí stav ověření. Tento stav by mohl naznačovat, že požadované konfigurace pro právnickou osobu nebyly dokončeny. Ze seznamu lze přejít přímo na stránky **Podrobnosti o uvolnění produktu**, **Údržba atributu produktu**, **Údržba kategorie produktu**, **Výchozí nastavení objednávky** a **Překlady textu** k dokončení nutných konfigurací produktu.

### <a name="manually-creating-a-new-released-product"></a>Ruční vytvoření nově uvolněného produktu

Uvolněný produkt můžete vytvořit ručně v jednom běhu, v závislosti na obchodních procesech dané organizace a pravidlech používání této funkce. Tato funkce vytvoří nový produkt a automaticky ho uvolní pro stávající právnickou osobu. Pokud chcete vytvořit nový produkt, klikněte na **Uvolněné produkty** v pracovním prostoru **Údržba uvolněných produktů** na stránce se seznamem **uvolněný produkt**.

