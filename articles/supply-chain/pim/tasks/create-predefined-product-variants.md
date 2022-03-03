---
title: Vytváření předdefinovaných variant produktů
description: Tento postup vás provede vytvořením variant produktu pro základní produkt za pomoci kombinací dimenzí produktu.
author: t-benebo
ms.date: 04/22/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart, EcoResProductVariantSuggestionsEnhanced
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6d3a4ae8efd438e01c263af1c0a1746d9484e491
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103082"
---
# <a name="predefined-product-variants"></a>Předdefinované varianty produktů

[!include [banner](../../includes/banner.md)]

## <a name="example-scenario-create-predefined-product-variants"></a>Příklad scénáře: Vytváření předdefinovaných variant produktů

Tento příklad scénáře vám ukáže, jak vytvořit varianty produktu pro základní produkt za pomoci kombinací dimenzí produktu.

### <a name="make-demo-data-available"></a>Zpřístupnění ukázkových dat

Pokud chcete provést tento scénář pomocí zde navržených hodnot, musíte mít nainstalována ukázková data a musíte vybrat právnickou osobu *USMF*.

### <a name="step-1-create-a-product-master"></a>Krok 1: Vytvoření základního produktu

Vytvoření základního produktu:

1. Přejděte do nabídky **Řízení informací o produktech > Produkty > Základní produkty**.
1. Zvolte **Nové**.
1. Pokud pole **Číslo produktu** již nezobrazuje číslo, pak zadejte hodnotu. Tento krok je vyžadován, jen pokud nebyla nastavena žádná číselná řada pro toto pole.
1. Do pole **Název produktu** zadejte název.
1. V poli **Skupina dimenzí produktu** vyberte skupinu dimenze produktu *SizeCol* (velikost a barva).
1. Vyberte **OK** k vytvoření a otevření nového hlavního produktu.

### <a name="step-2-add-product-dimensions"></a>Krok 2: Přidání dimenzí produktu

Tento příklad ukazuje, jak zadávat dimenze produktu ručně. Rovněž je možné vybrat velikost, barvu nebo skupinu stylů, která obsahuje hodnoty dimenze produktu, které chcete použít.

Přidání dimenzí produktu:

1. Když je nový hlavní produkt stále otevřený, vyberte **Rozměry produktu** v podokně akcí.
1. Otevřete kartu **Velikost** a vyberte **Nový** na panelu nástrojů pro přidání řádku do mřížky. Proveďte následující nastavení pro nový řádek:
    - **Velikost:** Vyberte hodnotu velikosti.
    - **Název**: Zadejte název velikosti.
1. Vyberte **Nový** na panelu nástrojů a přidejte do mřížky druhou velikost s novou hodnotou **Velikost** a **Název**.
1. Otevřete kartu **Barvy** a vyberte **Nový** na panelu nástrojů pro přidání řádku do mřížky. Proveďte následující nastavení pro nový řádek:
    - **Barva:** Vyberte hodnotu barvy.
    - **Název**: Zadejte název barvy.
1. Vyberte **Nový** na panelu nástrojů a přidejte do mřížky druhou barvu s novou hodnotou **Barva** a **Název**.
1. Zvolte **Uložit**.
1. Zavřete stránku a vraťte se k novému hlavnímu produktu.

### <a name="step-3-generate-product-variants"></a>Krok 3: Vytvoření variant produktů

> [!NOTE]
> Tato část popisuje, jak generovat varianty produktu, když funkce *Vylepšení stránky s návrhy variant* není povolena. V další části najdete podrobnosti o tom, jak generovat varianty produktu, když je tato funkce k dispozici.

Vytvoření variant produktů:

1. Když je nový hlavní produkt stále otevřený, vyberte **Varianty produktu** v podokně akcí.
1. V podokně Akce vyberte možnost **Návrhy variant**.
1. Systém generuje seznam všech možných kombinací velikostí a barev, které jste pro produkt definovali. Vyberte **Vybrat vše** na panelu nástrojů.
    - V tomto příkladu vyberte všechny možné varianty. Pokud chcete použít pouze podmnožinu možných kombinací dimenzí produktu, zaškrtněte podle potřeby pouze požadovaná zaškrtávací políčka.  
1. Vyberte **Vytvořit**.
1. Zvolte **Uložit**.

## <a name="improved-variant-suggestions"></a>Vylepšené návrhy variant

Funkce *Vylepšení stránky s návrhy variant* vylepšuje stránku **Návrhy variant** věnovanou problémům s výkonem a použitelností pro společnosti, které mají vysoký počet kombinací dimenzí produktů. Vylepšený proces výběru hodnot dimenzí produktu, pro které se generují návrhy variant, umožňuje rychlejší a snazší identifikaci a vydání příslušné sady variant produktu.

Tato funkce přidává následující vylepšení:

- **Odložené generování návrhů variant:** Stránka **Návrhy variant** již nezobrazuje návrhy při prvním otevření. Místo toho musíte explicitně zvolit, které hodnoty budete potřebovat, a poté vybrat tlačítko **Navrhnout** pro generování kombinací. Díky tomu je proces viditelnější a interaktivnější.
- **Výběr hodnot rozměrů:** Když máte mnoho hodnot dimenzí, obvykle vás zajímá generování návrhů variant, které obsahují jen několik z nich (například při zavádění nové sady barev nebo stylů). Díky vylepšenému designu můžete vybrat hodnoty dimenzí, pro které chcete generovat návrhy variant produktu. To značně zvyšuje relevanci navrhovaných variant a zlepšuje výkon systému i produktivitu uživatelů.

### <a name="turn-the-variant-suggestions-page-improvements-feature-on-or-off"></a>Zapnutí nebo vypnutí funkce Vylepšení stránky návrhů variant

Od verze Supply Chain Management 10.0.25 je tato funkce ve výchozím nastavení zapnuta. Správci mohou tuto funkci zapnout nebo vypnout vyhledáním funkce *Vylepšení stránky návrhů variant* v pracovním prostoru [Správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="work-with-the-improved-variant-suggestions"></a>Práce s vylepšenými návrhy variant

Vytváření návrhů variant produktu, když je funkce *Vylepšení stránky s návrhy variant* zapnutá:

1. Otevřete nebo vytvořte hlavní produkt a přidejte do něj požadované dimenze produktu, jak je popsáno v předchozí části.
1. Když je hlavní produkt otevřený, vyberte **Varianty produktu** v podokně akcí.
1. V podokně Akce vyberte možnost **Návrhy variant**.
1. Vyberte hodnoty, které chcete použít pro každou dimenzi.
1. Na horním panelu nástrojů vyberte **Navrhnout**.
1. Systém generuje seznam všech možných kombinací velikostí a barev, které jste vybrali. Na rychlé kartě **Navrhované varianty** zaškrtněte políčko pro každou kombinaci dimenze produktu, kterou chcete použít, nebo vyberte **Vybrat vše** na panelu nástrojů a vyberte je všechny.  
1. Vybrat **Vytvořit** k přidání variant do aktuálního hlavního produktu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
