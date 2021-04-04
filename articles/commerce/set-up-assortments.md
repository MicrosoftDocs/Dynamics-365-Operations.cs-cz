---
title: Nastavení sortimentu
description: Tento článek popisuje, co je sortiment, a vysvětluje, jak nastavit sortimenty v aplikaci Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d61addbc4eac691351c2d8cac013c9d94bd900e9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264593"
---
# <a name="set-up-assortments"></a>Nastavení sortimentu

[!include [banner](includes/banner.md)]

Tento článek popisuje, co je sortiment, a vysvětluje, jak nastavit sortimenty v aplikaci Dynamics 365 Commerce.

Sortiment je sada souvisejících produktů, které přiřadíte do velkoobchodní sítě, jako například kamenný obchod nebo online obchod. Sortimenty slouží k určení výrobků, které jsou k dispozici v každém obchodě. Sortiment může obsahovat kategorie produktů. Proto jsou v sortimentu zahrnuty všechny produkty, které jsou přiřazeny k vybrané kategorii. Sortiment může obsahovat také konkrétní produkty a varianty produktů. Nastavením sortimentu lze přiřadit tisíce produktů ke kanálům najednou, v libovolné kombinaci vyžadované obchodem. Lze nastavit tolik sortimentů produktů, kolik potřebujete. Každý výrobek může být zahrnut do jednoho nebo více sortimentů, a každý sortiment může být přiřazen jednomu nebo více kanálům. Například můžete definovat jeden sortiment zahrnující základní sadu produktů. Všechny obchody obdrží tento sortiment. Dále určíte jiný sortiment obsahující pouze velké sportovní zařízení. Pouze vyšší obchody obdrží tento sortiment. Následující diagram znázorňuje, jak mohou být výrobky přiřazeny k sortimentům, a jak lze tyto sortimenty přiřadit k prodejním kanálům.

![Vztahy sortimentů produktů](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Předpoklady

Než bude možné vytvořit sortiment a přiřadit jej do velkoobchodního kanálu, je třeba dokončit následující úkoly.

| Úkol                              | Popis |
|-----------------------------------|-------------|
| Nastavení kanálu.          | Prodejní kanály představují kamenný obchod, online obchod nebo třeba online tržiště. Musíte nastavit alespoň jeden prodejní kanál a nakonfigurovat možnosti úložiště. Sortimenty jsou přiřazeny k obchodům k identifikaci produktů, které určitý obchod nabízí. |
| Vytvořte organizační hierarchii. | Po nastavení velkoobchodních sítí v organizaci je nutné konfigurovat maloobchodní organizační hierarchii představující organizační strukturu maloobchodních kanálů. Hierarchii organizace lze použít pro sortiment, doplňování nebo výkaznictví. Přidáte-li prodejní kanály do organizační hierarchie, můžete přiřadit sortimenty ke skupinám obchodů. Namísto přiřazení sortimentů zvlášť pro každý obchod přiřaďte sortiment k nejvyšší úrovně uzlu organizace. Poté pokaždé, když je k uzlu organizace nejvyšší úrovně přidán nový prodejní kanál, daný prodejní kanál automaticky zdědí sortimenty, které byly přiřazeny k uzlu organizace vyšší úrovně. Můžete přiřadit pouze ty sortimenty k maloobchodním sítím, které jsou zahrnuty v organizační hierarchii, která je přiřazena k účelu **Velkoobchodní sortiment**. |
| Definujte produkty.                  | Předtím, než lze přidávat produkty do sortimentu, je třeba přidat je v aplikaci Commerce. Produkty lze přidávat ručně, nebo je můžete importovat od dodavatele. Po přidání produktů je musíte vydat právnické osobě. Pouze produkty, které byly uvolněny pro právnickou osobu, mohou být přidány do vašich kanálů. Produkty, které ještě nebyly uvolněny pro právnickou osobu, lze přidat do sortimentu, a sortiment může být schválen. Nicméně dokud produkty nebudou uvolněny pro právnické osoby, nemohou být přidány do prodejních kanálů. |
| Nastavení hierarchie kategorií.      | Při vytváření velkoobchodních produktů lze seskupit a kategorizovat je pomocí funkce hierarchie kategorií. Můžete vytvořit jednu hlavní hierarchii pro seskupení a kategorizování všech produktů, které distribuujete prostřednictvím vašich prodejních kanálů. Můžete také vytvořit samostatné doplňkové kategorie hierarchií k seskupení nebo kategorizaci produktů pro zvláštní účely, jako povýšení nebo sortimenty. Pomocí hierarchií kategorií můžete přiřadit všechny produkty v specifické kategorii k sortimentu. Všechny produkty, které jsou přidány do kategorie, která je zahrnuta v sortimentu, jsou automaticky zahrnuty do sortimentu. Poté při příštím spuštění plánovače sortimentu velkoobchodu budou tyto produkty k dispozici pro prodejní kanály, ke kterým je sortiment přiřazen. |

## <a name="setting-up-an-assortment"></a>Nastavení sortimentu

Po dokončení požadavků lze vytvořit sortiment a přiřadit jej do vašich prodejních kanálů. K vytvoření sortimentu je třeba dokončit následující úlohy.

1. Vytvořit nový sortiment nebo zkopírovat stávající sortiment.
2. Vyberte prodejní kanály nebo skupiny vysoké úrovně v prodejních kanálech, na které se sortiment vztahuje.
3. Přidejte do sortimentu kategorie produktů, jednotlivé produkty nebo varianty produktu. Všechny produkty lze zahrnout do konkrétní kategorie, nebo vyjmout vybrané produkty z kategorie, která je zahrnuta do sortimentu.
4. Publikujte sortiment. Při publikování sortimentu je automaticky spuštěn plánovač sortimentu. Tento proces generuje seznam produktů. Po dokončení tohoto procesu budou produkty k dispozici pro prodejní kanály, ke kterým je sortiment produktu přiřazen. Pokud jsou provedeny změny v publikovaném sortimentu nebo v prodejních kanálech, ke kterým je sortiment přiřazen, musí být sortiment aktualizován. Pokud chcete aktualizovat sortiment po provedení změn, můžete spustit plánovač sortimentu jako dávkovou úlohu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]