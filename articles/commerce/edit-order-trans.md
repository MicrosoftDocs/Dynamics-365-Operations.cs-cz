---
title: Úprava a audit online objednávky a asynchronních transakcí objednávek zákazníků
description: Toto téma popisuje, jak upravit a auditovat online objednávky a asynchronní transakce objednávek zákazníků v Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8fa6f7a71bae759e2b8feb3c5778200bb7bdbfe9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010144"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>Úprava a audit online objednávky a asynchronních transakcí objednávek zákazníků

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak upravit a auditovat online objednávky a asynchronní transakce objednávek zákazníků v Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Mezi verzemi Commerce 10.0.5 a 10.0.6 byla přidána podpora pro úpravy transakcí cash and carry (jako jsou prodeje a vrácení) a transakcí řízení hotovosti (jako je zadání plovoucího zůstatku a odstranění úhrad). V Commerce verze 10.0.7 byla přidána podpora pro úpravy transakcí online objednávek a asynchronních transakcí objednávek zákazníků.

## <a name="edit-and-audit-order-transactions"></a>Úprava a audit transakcí objednávek

Chcete-li upravit a auditovat transakce objednávek v Commerce Headquarters, postupujte takto.

1. Nainstalujte [doplněk Microsoft Dynamics Office](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Na stránce **Parametry maloobchodu** na záložce **Objednávky zákazníků** na záložce s náhledem **Objednávka** zadejte kód blokování pro **Kód blokování pro chyby synchronizace objednávky**.
1. Otevřete pracovní prostor **Finance obchodu**. Dlaždice **Chyby synchronizace online objednávek** a **Chyby synchronizace objednávek zákazníka** poskytují předfiltrované zobrazení stránky maloobchodních transakcí. Každé z nich zobrazuje záznamy transakcí, u kterých se nezdařila synchronizace pro odpovídající typ objednávky.
1. Otevřete buď stránku **Chyby synchronizace online objednávek** nebo stránku **Chyby synchronizace objednávek zákazníka**. Vyberte záznam a zobrazte podrobnosti chyby synchronizace. Záložka s náhledem **Stav synchronizace** poskytuje následující podrobnosti o chybě:

    - Stav čekající objednávky
    - Podrobnosti chyby objednávky
    - Datum a čas úpravy
    - Počet opakování

1. Pokud podrobnosti o chybě označují, že záznam musí být opraven, vyberte **Doplněk Office** a potom vyberte **Upravit vybranou transakci**. Otevře se soubor aplikace Excel, který zobrazuje podrobnosti vybrané transakce.

    - Pokud je upravovanou transakcí transakce online objednávky, soubor Excel obsahuje následující listy:

        - **Transakce** - Tento list obsahuje podrobnosti záhlaví transakce.
        - **Prodejní transakce** - Tento list obsahuje podrobnosti řádku transakce.
        - **Platební transakce** - Tento list obsahuje podrobnosti o řádcích platby dané transakce.
        - **Slevové transakce** - Tento list obsahuje podrobnosti transakce související se slevami.
        - **Daňové transakce** - Tento list obsahuje podrobnosti transakce související s daněmi.
        - **Transakce nákladů** - Tento list obsahuje data transakce související s náklady.

    - Pokud je upravovanou transakcí asynchronní transakce objednávek zákazníků, soubor Excel obsahuje následující listy:

        - **Řádky** - Tento list obsahuje podrobnosti záhlaví a řádku transakce.
        - **Platby** - Tento list obsahuje podrobnosti o řádcích platby dané transakce.
        - **Slevy** - Tento list obsahuje podrobnosti transakce související se slevami.
        - **Daně** - Tento list obsahuje podrobnosti transakce související s daněmi.
        - **Náklady** - Tento list obsahuje data transakce související s náklady.

1. V souboru Excel v poli **Čekající stav objednávky** zadejte **Úpravy** a poté publikujte změnu. Tímto způsobem zabráníte, aby úloha **Synchronizovat objednávku**, která běží v dávkovém režimu, přeskočila tento záznam během zpracování.
1. V souboru aplikace Excel upravte příslušná pole a poté odešlete data zpět do Commerce Headquarters pomocí funkce publikování doplňku Dynamics Excel. Po publikování dat se změny projeví v systému. Během publikování se neprovádí žádné ověření u změn, které uživatelé provedou.
1. Úplný záznam auditu změn lze zobrazit výběrem možnosti **Zobrazit záznam auditu** v záhlaví **Maloobchodní transakce** pro změny na úrovni záhlaví a v příslušné sekci a provést záznam na příslušné stránce transakce. Například všechny změny související s řádky prodeje se zobrazí na stránce **Prodejní transakce** a všechny změny související s platbami se zobrazí na stránce **Platební transakce**. Pro změny jsou zachovány následující podrobnosti auditu:

    - Datum a čas úpravy
    - Pole
    - Stará hodnota
    - Nová hodnota
    - Změnil/a

1. Po provedení a publikování změn vyberte **Synchronizovat objednávku** okamžitě zahájíte proces synchronizace. Alternativně můžete počkat, až proces synchronizace, který běží v dávkovém režimu, zpracuje transakci.

Ve výchozím nastavení se po úspěšné synchronizaci objednávek tyto objednávky dostanou do stavu blokace na základě kódu blokování, který je definován v parametrech Commerce. Blokování objednávek musí být odstraněno, než mohou být objednávky dále zpracovány pro plnění nebo jiné operace.

## <a name="additional-resources"></a>Další zdroje

[Úpravy a audit transakcí cash and carry a řízení hotovosti](edit-cash-trans.md)

[Úprava finančních dimenzí pro maloobchodní transakce](edit-financial-dim.md)

[Vytvoření sešitu aplikace Excel pro úpravu maloobchodních transakcí](create-excel-edit.md)

[Přidání polí do sešitu aplikace Excel pro úpravu maloobchodních transakcí](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]