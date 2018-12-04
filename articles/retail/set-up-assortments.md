---
title: "Nastavení sortimentu"
description: "Tento článek popisuje, co je sortiment, a vysvětluje, jak nastavit sortimenty v aplikaci Microsoft Dynamics 365 for Retail."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15811
ms.assetid: d2580048-e798-4b33-85f9-d1bad7d262fc
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 91713a4492ad82520f7dde611c17a5ea168ed80d
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-assortments"></a>Nastavení sortimentu

[!include [banner](includes/banner.md)]

Tento článek popisuje, co je sortiment, a vysvětluje, jak nastavit sortimenty v aplikaci Microsoft Dynamics 365 for Retail.

Sortiment je sada souvisejících produktů, které přiřadíte do maloobchodní sítě, jako například kamenný obchod nebo online obchod. Sortimenty slouží k určení výrobků, které jsou k dispozici v každém obchodě. Sortiment může obsahovat kategorie produktů. Proto jsou v sortimentu zahrnuty všechny produkty, které jsou přiřazeny k vybrané kategorii. Sortiment může obsahovat také konkrétní produkty a varianty produktů. Nastavením sortimentu lze přiřadit tisíce produktů k maloobchodním kanálům najednou, v libovolné kombinaci vyžadované obchodem. Lze nastavit tolik sortimentů produktů, kolik potřebujete. Každý výrobek může být zahrnut do jednoho nebo více sortimentů, a každý sortiment může být přiřazen jednomu nebo více maloobchodním kanálům. Například můžete definovat jeden sortiment zahrnující základní sadu produktů. Všechny obchody obdrží tento sortiment. Dále určíte jiný sortiment obsahující pouze velké sportovní zařízení. Pouze vyšší obchody obdrží tento sortiment. Následující diagram znázorňuje, jak mohou být výrobky přiřazeny k sortimentům, a jak lze tyto sortimenty přiřadit do maloobchodních sítí. ![Vztahy sortimentů produktů](./media/assortments_relationship.gif)

## <a name="prerequisites"></a>Požadavky
Než je možné vytvořit sortiment a přiřadit jej do maloobchodní sítě, je třeba vyplnit následující úlohy.

| Úkol                              | Popis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nastavení maloobchodního kanálu.          | Maloobchodní kanál představuje kamenný obchod, online obchod nebo třeba online tržiště. Musíte nastavit alespoň jednu maloobchodní síť a nakonfigurovat možnosti úložiště. Sortimenty jsou přiřazeny k obchodům k identifikaci produktů, které určitý obchod nabízí.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Vytvořte organizační hierarchii. | Po nastavení maloobchodních sítí v organizaci je nutné konfigurovat maloobchodní organizační hierarchii představující organizační strukturu maloobchodních kanálů. Hierarchii organizace lze použít pro sortiment, doplňování nebo výkaznictví. Přidáte-li maloobchodní kanály organizační hierarchie, můžete přiřadit sortimenty ke skupinám obchodů. Namísto přiřazení sortimentů zvlášť pro každý obchod přiřaďte sortiment k nejvyšší úrovně uzlu organizace. Poté pokaždé, když je k uzlu organizace nejvyšší úrovně přidána nová maloobchodní síť, daná maloobchodní síť automaticky zdědí sortimenty, které byly přiřazeny k uzlu organizace vyšší úrovně. Můžete přiřadit pouze ty sortimenty k maloobchodním sítím, které jsou zahrnuty v organizační hierarchii, která je přiřazena k účelu **Maloobchodní sortiment**. |
| Definujte produkty.                  | Předtím, než lze přidávat produkty do sortimentu, je třeba přidat je v aplikaci Microsoft Dynamics 365 for Retail. Produkty lze přidávat ručně, nebo je můžete importovat od dodavatele. Po přidání produktů je musíte vydat právnické osobě. Pouze produkty, které byly uvolněny pro právnické osoby, mohou být přidány do maloobchodních sítí. Produkty, které ještě nebyly uvolněny pro právnickou osobu, lze přidat do sortimentu, a sortiment může být schválen. Nicméně dokud produkty nebudou uvolněny pro právnické osoby, nemohou být přidány do maloobchodních sítí.                                                                                                                                                                                                                                                                                     |
| Nastavení hierarchie kategorií.      | Při vytváření maloobchodních produktů lze seskupit a kategorizovat je pomocí funkce hierarchie kategorií. Můžete vytvořit jednu hlavní hierarchii pro seskupení a kategorizování všech produktů, které distribuujete prostřednictvím prodejních kanálů. Můžete také vytvořit samostatné doplňkové kategorie hierarchií k seskupení nebo kategorizaci produktů pro zvláštní účely, jako povýšení nebo sortimenty. Pomocí hierarchií kategorií můžete přiřadit všechny produkty v specifické kategorii k sortimentu. Všechny produkty, které jsou přidány do kategorie, která je zahrnuta v sortimentu, jsou automaticky zahrnuty do sortimentu. Poté při příštím spuštění plánovače sortimentu maloobchodu budou tyto produkty k dispozici pro maloobchodní kanály, ke kterým je sortiment přiřazen.                                            |

## <a name="setting-up-an-assortment"></a>Nastavení sortimentu
Po dokončení požadavků lze vytvořit sortiment a přiřadit jej do vaší maloobchodní sítě. K vytvoření sortimentu je třeba dokončit následující úlohy.

1.  Vytvořit nový sortiment nebo zkopírovat stávající sortiment.
2.  Vyberte maloobchodní sítě nebo skupiny vysoké úrovně v maloobchodní síti, na které sortiment vztahuje.
3.  Přidejte do sortimentu kategorie produktů, jednotlivé produkty nebo varianty produktu. Všechny produkty lze zahrnout do konkrétní kategorie, nebo vyjmout vybrané produkty z kategorie, která je zahrnuta do sortimentu.
4.  Publikujte sortiment. Při publikování sortimentů je automaticky spuštěn plánovač maloobchodního sortimentu. Tento proces generuje seznam produktů. Po dokončení tohoto procesu budou produkty k dispozici pro maloobchodní kanály, ke kterým je sortiment produktu přiřazen. Pokud jsou provedeny změny v publikovaném sortimentu nebo v maloobchodní síti, ke které je sortiment přiřazen, musí být sortiment aktualizován. Pokud chcete aktualizovat sortiment po provedení změn, můžete spustit plánovač maloobchodního sortimentu jako dávkovou úlohu.





