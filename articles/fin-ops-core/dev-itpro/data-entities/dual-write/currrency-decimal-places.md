---
title: Migrace datového typu měny pro dvojitý zápis
description: Toto téma popisuje, jak změnit počet desetinných míst, která pro měnu podporuje duální zápis.
author: RamaKrishnamoorthy
ms.date: 04/06/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 62b24da65bfef64d54552e4a098941fee8c9bfd4
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416724"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Migrace datového typu měny pro dvojitý zápis

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Můžete zvýšit počet desetinných míst, která jsou podporována pro hodnoty měny, maximálně na 10. Výchozí limit jsou čtyři desetinná místa. Zvýšením počtu desetinných míst pomáháte zabránit ztrátě dat při synchronizaci dat pomocí duálního zápisu. Zvýšení počtu desetinných míst je změna typu opt-in. Chcete-li jej implementovat, musíte požádat o pomoc společnost Microsoft.

Proces změny počtu desetinných míst má dva kroky:

1. Žádost o migraci od společnosti Microsoft.
2. Změna počtu desetinných míst v Dataverse.

Aplikace Finance and Operations a Dataverse musí podporovat stejný počet desetinných míst v hodnotách měny. Jinak může dojít ke ztrátě dat, když jsou tyto informace synchronizovány mezi aplikacemi. Proces migrace překonfiguruje způsob uložení hodnot měny a směnného kurzu, ale nezmění žádná data. Po dokončení migrace lze zvýšit počet desetinných míst pro měnové kódy a ceny a data, která uživatelé zadávají a zobrazují, mohou mít větší desetinnou přesnost.

Migrace je volitelná. Pokud byste mohli mít podporu pro více desetinných míst, doporučujeme zvážit migraci. Organizace, které nevyžadují hodnoty, které mají více než čtyři desetinná místa, nemusí migrovat.

## <a name="requesting-migration-from-microsoft"></a>Žádost o migraci od společnosti Microsoft

Úložiště pro existující měnové sloupce v Dataverse nemůže podporovat více než čtyři desetinná místa. Proto během procesu migrace jsou hodnoty měny zkopírovány do nových interních sloupců v databázi. Tento proces probíhá nepřetržitě, dokud nebudou migrována všechna data. Interně na konci migrace nové typy úložišť nahrazují staré typy úložišť, ale hodnoty dat se nezmění. Sloupce měny pak mohou podporovat až 10 desetinných míst. Během procesu migrace lze Dataverse nadále používat bez přerušení.

Současně jsou měnové kurzy upravovány tak, aby podporovaly až 12 desetinných míst místo současného limitu 10. Tato změna je nutná, aby počet desetinných míst byl stejný v aplikaci Finance and Operations a Dataverse.

Migrace nezmění žádná data. Po převodu sloupců měny a směnného kurzu mohou správci nakonfigurovat systém tak, aby používal až 10 desetinných míst pro měnové sloupce zadáním počtu desetinných míst pro každou měnu transakce a pro stanovení ceny.

### <a name="request-a-migration"></a>Požádejte o migraci

Tuto funkci zpřístupníte odesláním e-mailu na **CDSExpandDecimal@microsoft.com** a obsahují následující informace:

+ **Předmět:** Žádost o povolení rozšířené desetinné podpory pro \<organizationID\>
+ **Text:** Chtěl bych povolit rozšířenou desetinnou podporu pro moji organizaci \<organizationID\>.

Zástupce společnosti Microsoft vás bude kontaktovat do dvou až tří pracovních dnů pro další kroky.

Když požádáte o migraci, měli byste znát následující podrobnosti a podle toho je naplánovat:

+ Čas potřebný k migraci dat závisí na množství dat v systému. Migrace velkých databází může trvat několik dní.
+ Velikost databáze se během migrace dočasně zvyšuje, protože pro indexy je potřeba další místo. Po dokončení migrace je většina volného místa uvolněna.
+ Pokud během procesu migrace dojde k chybám, které brání dokončení migrace, systém upozorní podporu společnosti Microsoft, aby mohli pracovníci podpory zasáhnout. I když se však během migrace vyskytnou chyby, Dataverse zůstává plně k dispozici pro pravidelné používání.
+ Proces migrace není reverzibilní.

## <a name="changing-the-number-of-decimal-places"></a>Změna počtu desetinných míst

Po dokončení migrace Dataverse může ukládat čísla, která mají více desetinných míst. Správci si mohou vybrat, kolik desetinných míst se použije pro konkrétní kódy měn a pro stanovení ceny. Uživatelé Microsoft Power Apps, Power BI, a Power Automate pak mohou zobrazit a používat čísla, která mají více desetinných míst.

Chcete-li provést tuto změnu, musíte aktualizovat následující nastavení v aplikaci Power Apps:

+ **Systémová nastavení: Přesnost měny pro stanovení ceny** - sloupec **Nastavit přesnost měny, která se používá pro stanovení cen v celém systému** definuje, jak se bude měna chovat pro organizaci, když je vybrána **Přesnost stanovení cen**.
+ **Řízení podniku: měny** - sloupec **Přesnost měny** umožňuje určit vlastní počet desetinných míst pro konkrétní měnu. Existuje nastavení pro celou organizaci.

Existují některá omezení:

+ Nelze konfigurovat sloupec měny v tabulce.
+ Více než čtyři desetinná místa můžete zadat pouze na úrovni **Stanovení ceny** a **Měna transakce**.

### <a name="system-settings-currency-precision-for-pricing"></a>Systémová nastavení: Přesnost měny pro stanovení ceny

Po dokončení migrace mohou správci nastavit přesnost měny. Přejděte na **Nastavení \> Správa** a vyberte **Nastavení systému**. Pak na kartě **Obecné** změňte hodnotu sloupce **Nastavit přesnost měny, který se používá pro stanovení cen v celém systému**, jak je znázorněno na následujícím obrázku.

![Systémová nastavení měny.](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>Řízení podniku: měny

Pokud požadujete, aby se přesnost měny pro konkrétní měnu lišila od přesnosti měny použité pro stanovení ceny, můžete ji změnit. Přejděte na **Nastavení \> Řízení podniku**, vyberte **Měny** a vyberte měnu, kterou chcete změnit. Pak nastavte sloupec **Přesnost měny** a zadejte požadovaný počet desetinných míst, jak je znázorněno na následujícím obrázku.

![Nastavení měny pro konkrétní národní prostředí.](media/specific-currency.png)

### <a name="tables-currency-column"></a>tabulky: Sloupec Měna

Počet desetinných míst, která lze konfigurovat pro konkrétní sloupce měny, je omezen na čtyři.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]