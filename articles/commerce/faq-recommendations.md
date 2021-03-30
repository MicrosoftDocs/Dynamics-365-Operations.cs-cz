---
title: Často kladené dotazy k doporučení produktu
description: Toto téma obsahuje informace o procesech a nástrojích, které lze použít při řešení problémů souvisejících s doporučeními produktů nebo s jejich výsledky.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f0140f798e000ca66c67afa00f788abc560c8a07
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216692"
---
# <a name="product-recommendations-faq"></a>Často kladené dotazy k doporučení produktu


[!include [banner](includes/banner.md)]

Toto téma obsahuje informace o procesech a nástrojích, které lze použít při řešení problémů souvisejících s [doporučeními produktů](product-recommendations.md) nebo s jejich výsledky.

## <a name="best-practices"></a>Doporučené postupy
Je velmi důležité používat koncept základních produktů a variant. Praktické seskupení variant do nadřazeného základního produktu pomáhá vytvářet algoritmy a služby pro lepší modely. Kromě toho může služba obsloužit pouze jednu instanci produktu namísto vkládání všech úzce souvisejících variant do seznamu. Když jsou všechny úzce související varianty vloženy do seznamu, může dojít k chybám nebo duplicitním výsledkům.

## <a name="why-are-products-missing-from-my-recommendation-lists"></a>Proč v seznamech doporučení chybějí produkty?

Obyčejně pokud v seznamu doporučení produktů chybí některá položka, může se jednat o problém s konfigurací produktu. Může se například jednat o nesprávné počáteční nebo koncové datum produktu, může být nesprávně nakonfigurován rozměr nebo se produkt nemusí nacházet ve správném sortimentu kanálů atd.

Pokud položka chybí v seznamu doporučení, který vychází ze strojového učení na bázi umělé inteligence (AI-ML), položka pravděpodobně nesplňuje kritéria seznamu doporučení nebo nemá dostatek nákupních transakcí pro seznam doporučení, aby ji bylo možné zobrazit.

Doporučujeme, abyste provedli kontrolu následujících kroků:
1. **Zkontrolujte, zda byla v centrále povolena doporučení produktu.** Další informace o povolení této služby naleznete v tématu [Povolení doporučení produktů](enable-product-recommendations.md).
1. **Zkontrolujte, zda jsou nastaveny klíčové vlastnosti produktu.** Například sortimenty výrobků musí být nastaveny tak, aby byly **zahrnuty**.
1. **U nově roztříděných produktů může trvat až 3 hodiny, než se produkt začne zobrazovat v novém seznamu.**
1. **Pokud se produkt stále nezobrazuje v seznamech V kurzu, Nejprodávanější, Lidem se také líbí nebo Často zakoupeno společně, je možné, že tento produkt nemá dostatek transakcí.** V takovém případě můžete počkat, až se vyskytnou další transakce, aktualizovat výchozí parametry seznamu doporučení nebo pomocí ručního zásahu upravit výsledky seznamu doporučení produktů. Další informace o parametrech doporučení naleznete v tématu [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).
1. **Ujistěte se, že produkt splňuje kritéria doporučení pro daný seznam.** Další informace o parametrech doporučení produktů naleznete v tématu [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a>Jak lze zabránit vrácení špatných výsledků doporučení?

Seznamy doporučení vyžadují k vytvoření výsledků velký objem transakcí. Proto je důležité, aby uživatelé poskytovali úplná historická data transakcí.

Dále produkty, které nemají žádné nebo málo transakcí, obvykle nedosahují výsledků **Lidem se také líbí** nebo **Často zakoupeno společně** a nezobrazují se v seznamech doporučení **V kurzu** nebo **Nejprodávanější**. Tato situace může často nastat u velmi nových nebo u starých produktů, které mají malý počet nákupů. Populární nové položky snadno vyřeší tento problém.

Doporučujeme, abyste se řídili následujícími kroky:
1. **Ujistěte se, že produkt splňuje kritéria doporučení pro daný seznam.** Další informace o parametrech doporučení produktů naleznete v tématu Úprava výsledků doporučení produktů na základě umělé inteligence a strojového učení.
1. **Je-li produkt nový, zvažte úpravu seznamu doporučení, dokud produkt nemá více transakcí.** Další informace o úpravách výsledků seznamu doporučení naleznete v tématu [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).


- **Ujistěte se, že produkt splňuje kritéria doporučení pro daný seznam.** Další informace o parametrech doporučení produktů naleznete v tématu [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).
- **Je-li produkt nový, zvažte úpravu seznamu doporučení, dokud produkt nemá více transakcí.** Další informace o úpravách výsledků seznamu doporučení naleznete v tématu [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a>Mohu produkt odebrat, aby se přesto zobrazoval v obchodě?

Můžete upravit seznamy, které jsou algoritmicky vygenerovány v případě obchodní potřeby. Pokud je však produkt odebrán ze seznamu doporučení, bude produkt v obchodě stále vyhledatelný. Další informace o úpravách výsledků doporučení produktů naleznete v tématu [Správa výsledků doporučení produktů na základě umělé inteligence a strojového učení](modify-product-recommendation-results.md).

Pokud je nutné blokovat určitou položku v obchodě, aby ji nebylo možné vyhledat, je nutné změnit hodnotu **Sortimenty položek** tak, aby byla **vyloučena**.

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a>Jak lze přidat seznam na stránku elektronického obchodu?

Informace o tom, jak přidat stránky doporučení produktů na web elektronického obchodování, naleznete v tématu [Přidání seznamů doporučení produktů na stránky](add-reco-list-to-page.md).

## <a name="how-do-i-enable-recommendations-on-pos"></a>Jak lze povolit doporučení v POS?

Po povolení doporučení produktů budete muset přidat panel doporučení na řídicí obrazovku POS. Další informace viz [Přidání ovládacího prvku doporučení na obrazovku transakce na zařízeních POS](add-recommendations-control-pos-screen.md).

## <a name="additional-resources"></a>Další prostředky

[Přehled doporučení produktu](product-recommendations.md)

[Povolení Azure Data Lake Storage v prostředí Dynamics 365 Commerce](enable-adls-environment.md)

[Povolit doporučení produktu](enable-product-recommendations.md)

[Povolení přizpůsobených doporučení](personalized-recommendations.md)

[Odhlášení přizpůsobených doporučení](personalization-gdpr.md)

[Povolit doporučení typu „podobný vzhled“](shop-similar-looks.md)

[Přidání doporučení produktu v POS](product.md)

[Přidání doporučení na obrazovku transakcí](add-recommendations-control-pos-screen.md)

[Úprava výsledků doporučení AI-ML](modify-product-recommendation-results.md)

[Ručně vytvořit uspořádaná doporučení](create-editorial-recommendation-lists.md)

[Vytvořit doporučení s ukázkovými daty](product-recommendations-demo-data.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]