---
title: Úprava a audit online objednávky a asynchronních transakcí objednávek zákazníků
description: Tento článek popisuje, jak upravit a auditovat online objednávky a asynchronní transakce objednávek zákazníků v Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 10/21/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: dbeeff47446c1617da44f34ae56f333717f577a1
ms.sourcegitcommit: 18b7a02c497709e8d9c7b943d82f1fcc3dafa4cd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/21/2022
ms.locfileid: "9712101"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a>Úprava a audit online objednávky a asynchronních transakcí objednávek zákazníků

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak upravit a auditovat online objednávky a asynchronní transakce objednávek zákazníků v Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Mezi verzemi Commerce 10.0.5 a 10.0.6 byla přidána podpora pro úpravy transakcí cash and carry (jako jsou prodeje a vrácení) a transakcí řízení hotovosti (jako je zadání plovoucího zůstatku a odstranění úhrad). V Commerce verze 10.0.7 byla přidána podpora pro úpravy transakcí online objednávek a asynchronních transakcí objednávek zákazníků.

## <a name="edit-and-audit-order-transactions"></a>Úprava a audit transakcí objednávek

Pokud chcete upravit a auditovat transakce objednávek v Commerce Headquarters, postupujte následovně.

1. Nainstalujte [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).
1. Na stránce **Parametry Commerce** na kartě **Objednávky zákazníků** na záložce s náhledem **Objednávka** zadejte kód blokování pro **Kód blokování pro chyby synchronizace objednávky**.
2. Pozastavte jiné úlohy synchronizace objednávek, které budou v rozporu s načasováním vašich úprav a auditu.
3. Otevřete pracovní prostor **Finance obchodu**. Dlaždice **Chyby synchronizace online objednávek** a **Chyby synchronizace objednávek zákazníka** poskytují předfiltrované zobrazení stránky maloobchodních transakcí. Každé z nich zobrazuje záznamy transakcí, u kterých se nezdařila synchronizace pro odpovídající typ objednávky.
4. Otevřete buď stránku **Chyby synchronizace online objednávek** nebo stránku **Chyby synchronizace objednávek zákazníka**. Vyberte záznam a zobrazte podrobnosti chyby synchronizace. Záložka s náhledem **Stav synchronizace** poskytuje následující podrobnosti o chybě:

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
1. V souboru aplikace Excel upravte příslušná pole a poté odešlete data zpět do Commerce Headquarters pomocí funkce publikování doplňku Dynamics Excel. Po publikování dat se změny projeví v systému. Během publikování se neprovádí žádné ověřování změn provedených uživateli.
    > [!NOTE]
    > Pokud nemůžete najít pole, které potřebujete upravit, přidejte chybějící pole do listu podle následujících kroků.
    >   1. Vyberte možnost **Design** u položky Datový konektor.
    >   1. Vyberte ikonu tužky vedle tabulky, do které chcete přidat pole.
    >   1. Vyberte pole v sekci **Dostupná pole** a poté vyberte možnost **Přidat**.
    >   1. Přidejte požadovaný počet polí a poté vyberte možnost **Aktualizovat**.
    >   1. Po dokončení aktualizace může být nutné zvolit možnost **Aktualizovat**, aby došlo k aktualizaci hodnot.

3. Úplný záznam auditu změn lze zobrazit výběrem možnosti **Zobrazit záznam auditu** v záhlaví **Maloobchodní transakce**. Můžete zobrazit změny na úrovni záhlaví a v příslušné sekci a provést záznam na příslušné stránce transakce. Například všechny změny související s řádky prodeje se zobrazí na stránce **Prodejní transakce** a všechny změny související s platbami se zobrazí na stránce **Platební transakce**. Pro změny jsou zachovány následující podrobnosti auditu:

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
