---
title: Spravujte změny v recepturách a jejich látkách
description: Tento článek popisuje, jak provádět správu vzorců a spravovat změny ve zpracování hlavních dat výroby.
author: t-benebo
ms.date: 05/19/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-19
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8105ebc7f3698a6baaa04b6548dac18a7bf81a47
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904065"
---
# <a name="manage-changes-in-formulas-and-their-ingredients"></a>Spravujte změny v recepturách a jejich látkách

[!include [banner](../includes/banner.md)]

Pokud používáte výrobní možnosti Microsoft Dynamics 365 Supply Chain Management, můžete také použít související možnosti správy vzorců ke správě následujících změn:

- **Vzorec a položky plánování:** Spravujte změny složek ve vzorcích a jejich vedlejších a vedlejších produktech.
- **Souběžné produkty a vedlejší produkty:** Upravte množství a další informace o souběžných produktech a vedlejších produktech v receptuře.
- **Položky se skutečnou hmotností:** Spravujte změny u položek se skutečnou hmotností.

## <a name="turn-this-feature-on-or-off"></a>Zapnutí nebo vypnutí této funkce

Funkce popsané v tomto článku vyžadují, aby byly na vašem systému zapnuty funkce *Správa technických změn* a *Správa změn v recepturách a jejich látkách*. Podrobnosti o tom, jak tyto funkce zapnout nebo vypnout, najdete v tématu [Přehled správy technických změn](product-engineering-overview.md).

## <a name="feature-naming-conventions"></a>Konvence pojmenování funkcí

V uživatelském rozhraní (UI) Supply Chain Management a dokumentaci se funkce správy změn obvykle označuje jako *řízení technických změn* a spravovatelné produkty se obvykle označují jako *strojírenské produkty*. Ačkoli tato terminologie není obvykle spojena se správou receptur pro procesní výrobu, měli byste považovat správu technických změn za jednoduše správu změn a měli byste považovat technické produkty za produkty s verzí.

## <a name="work-with-formula-change-management-features"></a>Práce s funkcemi pro správu změn receptur

Následující seznam shrnuje, jak se funkce správy technických změn vztahují na správu receptur. Poskytuje také odkazy na další informace. Vzhledem k tomu, že správa změn receptur využívá funkce správy technických změn, měli byste se naučit, jak správa technických změn obecně funguje, abyste ji mohli použít ke správě receptur a jejich látek.

- **Centralizovaná správa produktových dat** - Vytvořte organizaci, která prostřednictvím procesu řízeného uvolnění zajistí, aby uživatelům v celém podniku byly k dispozici přesné a relevantní údaje o produktu. Další informace viz [Pravidla technických společností a vlastnictví dat](engineering-org-data-ownership-rules.md).
- **Verzování produktu** - Sledujte změny produktů prostřednictvím verzí produktů a kontrolujte produkt ve všech fázích dodavatelského řetězce. Tímto způsobem můžete sledovat změny ve svých formulacích. Více informací naleznete v části [Technické verze a kategorie technických produktů](engineering-versions-product-category.md).
- **Správa životního cyklu produktu** - Spravujte viditelnost údajů o produktech v celé organizaci a kontrolujte dostupnost verzí produktů v každé fázi dodavatelského řetězce. Máte podrobnou kontrolu nad tím, kdy lze verzi produktu použít v konkrétních obchodních procesech, a můžete si vytvořit svůj vlastní stav životního cyklu, který odpovídá vašim obchodním potřebám. Další informace viz [Stavy životního cyklu produktu a transakce](product-lifecycle-state-transactions.md).
- **Řízení změn receptur** - Uživatelé v celé vaší organizaci mohou požadovat změny receptur. Pomocí objednávek změn můžete vyhodnotit a dokumentovat dopad navrhovaných změn. Přidejte pracovní postupy pro správu procesu změn a vydání nových verzí produktu a jeho receptury. Další informace naleznete v tématu [Správa změn technických produktů](engineering-change-management.md).
- **Kontrola připravenosti** - Pomocí systémových kontrol a pokynů uživatele (dotazníky a kontrolní seznamy) zajistěte, aby byla před vydáním produktu plně zadána všechna požadovaná data o produktu. Další informace naleznete v tématu [Připravenost produktu](product-readiness.md).
- **Vylepšená funkce vydání produktu** - Vydejte plně definované verze produktu a jeho receptury z organizace (právnické osoby) do jiných právnických osob. Můžete dokonce rozhodnout, zda musí být informace o produktu před vydáním zkontrolovány nebo upraveny. Další informace naleznete v tématu [Vydání struktur produktu](release-product-structure.md).

Všimněte si, že většina článků, na která se odkazuje v předchozím seznamu, poskytuje příklady založené na kusovnících (BOM). Vzorce však fungují podobným způsobem. Zde je několik dalších konceptů, které je užitečné znát, když ke správě receptur a kusovníků používáte správu změn (nebo pouze správu změn receptur):

- Pro každou [technockou kategorii produktů](engineering-versions-product-category.md) můžete určit typ výroby (kusovník, receptura nebo položka plánování). Můžete také určit, zda je u produktů, které tuto kategorii používají, požadována podpora hmotnosti.
- Souběžné produkty a vedlejší produkty nejsou technické produkty. Proto nemají verzované. Pokud je musíte změnit, jednoduše vytvořte nový produkt. Tento přístup usnadňuje údržbu.
- Můžete spravovat koncové položky, které jsou kusovníky a které mají podřízené položky receptur. Tato funkce bude fungovat pro jakoukoli kombinaci kusovníků, které obsahují receptury a/nebo receptury, které obsahují kusovníky.
