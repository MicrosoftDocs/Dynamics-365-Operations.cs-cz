---
title: Přehled zásobovacího katalogu
description: Tento článek popisuje na nejvyšší úrovni, jak mohou odborníci na nákup nastavit a spravovat zásobovací katalogy. Zásobovací katalogy definují položky a služby, které zaměstnanci společnosti mohou objednat pro interní použití.
author: GalynaFedorova
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, CatDisplayProductRelationAdd
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2214"
- intro-internal
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd267cbbe7767faab538cacad26636ff1f37a551
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672003"
---
# <a name="procurement-catalogs-overview"></a>Přehled zásobovacího katalogu

[!include [banner](../includes/banner.md)]

Tento článek popisuje na nejvyšší úrovni, jak mohou odborníci na nákup nastavit a spravovat zásobovací katalogy. Zásobovací katalogy definují položky a služby, které zaměstnanci společnosti mohou objednat pro interní použití.

Nákupčí mohou vytvářet a udržovat katalogy položek a služeb, které lze zakoupit pro interní použití v organizaci. Po nastavení katalogů může zaměstnanec společnosti vytvořit nákupní žádanky k vytvoření objednávky. Katalogy lze použít k vynucení zásady nákupu, aby zaměstnanci mohli objednat pouze položky a služby, které jsou povoleny pro jejich kupující právnickou osobu. Při vytváření zásobovacího katalogu doporučujeme zvážit provedení následujících úkolů:

-   Vytvořte hierarchii kategorií zásobování před vytvořením katalogu.
-   Určete produkty, které chcete mít objednané vašimi zaměstnanci. Můžete zobrazit nebo skrýt určité produkty v uzlu katalogu nebo můžete zobrazit nebo skrýt všechny produkty v uzlu.
-   Určete, kolik zásobovacích katalogů požadujete. Přístup k zásobovacímu katalogu je určen pravidly zásad katalogu, který konfigurujete pro právnickou osobu a provozní jednotky, která je přiřazena konkrétnímu zaměstnanci.

To, které produkty, mohou zaměstnanci objednávat, a které kategorie zásobování mohou používat při vytváření nákupních žádanek, je určeno několika faktory:

-   Pravidlo zásad přístupu ke kategorii v zásadě nákupu určuje, které kategorie zásobování jsou k dispozici v nákupní žádance. Pokud není definováno žádné pravidlo, jsou k dispozici všechny kategorie zásobování.
-   Zaměstnanci mohou objednat produkt, pouze pokud je v aktivním zásobovacím katalogu pro organizaci a pokud je v povoleném uzlu a není skrytý. Produkt musí také být v kategorii, do které má určitý zaměstnanec přístup podle pravidla zásad přístupu ke kategorii.
-   Pravidlo zásad katalogu určuje katalog, který se používá. Pokud nezadáte žádné pravidlo zásad katalogu, samotné pravidlo přístupu ke kategorii určuje produkty, které zaměstnanec může objednat na žádance.

## <a name="prerequisites"></a>Požadavky
V následující tabulce jsou uvedeny úkoly, které je nutné dokončit před tím, než pracovník nákupu může vytvořit zásobovací katalog.

| Úkol                                                | Role               | Popis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nastavte hierarchii kategorií zásobování.            | Manažer nákupu | Hierarchie kategorií zásobování se používají ke klasifikaci položek nebo transakcí pro vykazování a analýzy. Pomocí hierarchie kategorií zásobování společností lze strategicky spravovat kategorie, výrobky, dodavatele a další činitele zásobování z centrálního umístění. Pro celou organizaci lze definovat pouze jednu hierarchii kategorií zásobování. Katalog vychází z hierarchie kategorií zásobování: kategorie v hierarchii se v katalogu stanou uzly. Dodavatelé a produkty jsou zahrnuté v katalogu. |
| Přidejte dodavatele a produkty do kategorií zásobování. | Manažer nákupu | Když je pro vaši organizaci vytvořena hierarchie kategorií zásobování, může být každá zásobovací kategorie přiřazena specifickému dodavateli, produktu apod. Tato přidružení se zkopírují automaticky do katalogu.                                                                                                                                                                                                                                                                                           |

## <a name="setting-up-a-catalog"></a>Nastavení katalogu.
Poté, co byly splněny požadavky, můžete nastavit katalogy. Můžete vytvořit jeden katalog, který se používá v celé organizaci, nebo více katalogů, které používají různé divize v organizaci. Pokud vytvoříte jeden katalog pro celou organizaci, přístup do katalogu je řízen pravidly zásad nákupu.  

Katalog definuje, které produkty jsou k dispozici při vytváření nákupních žádanek, můžete ale použít pravidla zásad přístupu ke kategorii k uplatnění dalších omezení. Vzhledem k tomu, že uzly v katalogu jsou kategorie zásobování, lze je potlačit pravidlem zásad přístupu ke kategorii. V takovém případě nejsou produkty v této kategorii nejsou k dispozici, aby je zaměstnanci mohli používat na žádankách. Pravidla zásad přístupu ke kategorii definujete na stránce **Zásady nákupu**. V následující tabulce jsou popsány úkony, které je nutné dokončit pro nastavení katalogu.

| Úkol                                                   | Role             | Popis                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vytvořte nový katalog.                                  | Nákupčí | Při vytváření katalogu je třeba zadat název a popis pro katalog. Také definujete, zda se katalog aktualizuje ručně nebo automaticky, a zadáváte vlastníka katalogu.                                                                                                                                      |
| Určete, zda jsou produkty k dispozici v katalogu. | Nákupčí | Vzhledem k tomu, že jsou produkty převzaty z kategorií zásobování, všechny se zobrazují v příslušných uzlech katalogu. Můžete určit, zda jsou všechny produkty v uzlu skryté nebo zobrazené, když je katalog použit nákupní žádance. Můžete také určit, zda jednotlivé produkty v uzlu jsou skryté nebo zobrazené. |
| Publikujte katalog.                                   | Nákupčí | Dříve, než bude katalog k dispozici zaměstnancům pro použití v žádance, musíte definovat pravidlo zásad katalogu pro daný katalogu, nastavit stav katalogu na hodnotu **Aktivní** a katalog pak publikovat. Můžete deaktivovat katalogy, u kterých nechcete, aby byly nadále uživatelům k dispozici.                                              |

Aktualizace jsou publikovány automaticky nebo ručně v závislosti na možnosti vybrané v poli **Výchozí typ aktualizace** na stránce **Katalogy**. K dispozici pro katalogy jsou následujících výchozích typy aktualizace:

-   **Dynamická**: Katalog se automaticky aktualizuje pokaždé, když se změní.
-   **Statická**: Katalog musíte aktualizovat ručně.
-   **Obě**: Pokud katalog zahrnuje kategorie produktů, které mají výchozí typ aktualizace **Statická**, je nutné je aktualizovat ručně při aktualizaci těchto kategorií. Pokud katalog zahrnuje kategorie produktů, které mají výchozí typ aktualizace **Dynamická**, aktualizuje se automaticky pokaždé, když se změní.


## <a name="additional-resources"></a>Další zdroje

[Nastavení hierarchie kategorií zásobování](tasks/set-up-procurement-category-hierarchy.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]