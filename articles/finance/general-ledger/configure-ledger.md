---
title: Konfigurace hlavních knih
description: Toto téma poskytuje informace o tom, jak konfigurovat hlavní knihy pro každou právnickou osobu. Zahrnuje informace o tom, jak vybrat měny, fiskální kalendáře, účtovou osnovu a účetní struktury, které by se měly používat u každé právnické osoby.
author: kweekley
ms.date: 09/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Ledger
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-09
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 38c4364c47915cc0019cb6b3d471d3e60d413bf0
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711541"
---
# <a name="configure-ledgers"></a>Konfigurace hlavních knih

[!include [banner](../includes/banner.md)]

Toto téma poskytuje informace o tom, jak konfigurovat hlavní knihy pro každou právnickou osobu. Zahrnuje informace o tom, jak vybrat měny, fiskální kalendáře, účtovou osnovu a účetní struktury, které by se měly používat u každé právnické osoby.

## <a name="selecting-the-chart-of-accounts"></a>Výběr účtové osnovy

Pro každou právnickou osobu v Microsoft Dynamics 365 Finance je třeba nakonfigurovat podrobnosti o hlavní knize. Stránka **Hlavní kniha** umožňuje vybrat účtovou osnovu a účetní struktury, které budou použity pro vybranou právnickou osobu. Svou účtovou osnovu a účetní struktury můžete sdílet konfigurací stránky **Hlavní kniha** u každé právnické osoby, abyste používali stejnou účtovou osnovu a účetní struktury. Můžete také sdílet část konfigurace pro každou právnickou osobu a mít konkrétní konfigurace u každé právnické osoby.

Pokud vaše právnické osoby musí mít různé účetní osnovy nebo různé účetní struktury, může být užitečná funkce přepsání právnických osob. Použitím stejné účetní osnovy a účetní struktury pro více právnických osob a následnou správou libovolných výjimek prostřednictvím přepsání právnických osob můžete časem zjednodušit údržbu.

Chcete-li nakonfigurovat účtovou osnovu pro právnickou osobu, přejděte na **Hlavní kniha \> Nastavení hlavní knihy \> Hlavní kniha**. Na stránce **Hlavní kniha** vyberte **Účtová osnova** a poté v seznamu vyberte účtovou osnovu, kterou chcete použít. Upozorňujeme, že účetní osnovu nelze změnit, když vyberete hodnotu a zaúčtujete transakce v právnické osobě.

Další informace, jak plánovat a konfigurovat účtovou osnovu a hlavní účty, najdete v části [Plánování účtové osnovy](plan-chart-of-accounts.md).

## <a name="selecting-account-structures"></a>Výběr účetních struktur

Každá právnická osoba v Dynamics 365 Finance lze nakonfigurovat pro použití jedné nebo více účetních struktur. Každá účetní struktura definuje finanční dimenze a kombinace hlavních účtů a finančních dimenzí, které budou povoleny při zaúčtování transakcí. Stejné účetní struktury můžete použít ve více než jedné právnické osobě.

Upozorňujeme, že pokud máte více účetních struktur, můžete vybrat pouze účetní struktury, které nemají překrývající se kombinace hlavních účtů a finančních dimenzí. Například jedna z vašich účetních struktur je nakonfigurována tak, aby přidávala obchodní jednotku pro hlavní účty mezi 1000 a 1999. V jiné účetní struktuře jste přidali finanční dimenzi Oddělení pro hlavní účty, které začínají 1. V takovém případě lze ke stejné právnické osobě přidat pouze jednu z účetních struktur.

Chcete-li nakonfigurovat účetní struktury pro svou hlavní knihu, na stránce **Účetní kniha** na záložce s náhledem **Účetní struktury** vyberte **Přidat**, vyberte účetní strukturu v seznamu a poté vyberte **Vybrat**. Přidání a uložení účetních struktur může trvat několik minut. Upozorňujeme, že účetní struktury, které vyberete, musí být aktivní. V opačném případě nebudou podrobnosti účetních struktur účinné u právnických osob, se kterými jsou propojeny.

Chcete-li odstranit účetní strukturu, na stránce **Hlavní kniha** na záložce s náhledem **Účetní struktury** vyberte **Odebrat**. Všimněte si, že pokud odeberete účetní strukturu z hlavní knihy, neodstraníte žádné transakce, které byly zaúčtovány pomocí konfigurace této účetní struktury.

Další informace, jak nastavit účetní struktury, najdete v části [Konfigurace účetních struktur](configure-account-structures.md).

## <a name="configuring-calendars-for-the-ledger"></a>Konfigurace kalendářů pro hlavní knihu

Další součástí hlavní knihy je fiskální kalendář. Fiskálního kalendář je třeba vybrat pro každou právnickou osobu. Stejný fiskální kalendář můžete použít ve více než jedné právnické osobě. Když vyberete fiskální kalendář pro hlavní knihu, vytvoří se kopie. Tato kopie se označuje jako kalendář hlavní knihy. Kalendář hlavní knihy umožňuje vybrat stav období a moduly v každém období.

Pro přístup a aktualizaci kalendáře pro vybranou právnickou osobu na stránce **Hlavní kniha** v podokně akcí vyberte **Kalendář hlavní knihy**.

Chcete-li vybrat kalendář, vyberte **Fiskální kalendáře** a poté vyberte kalendář v seznamu. Pokud změníte fiskální kalendář po zaúčtování transakcí v právnické osobě, musíte vybrat **Přepočítat období hlavní knihy**. V zobrazeném dialogovém okně můžete aktualizovat zůstatky hlavní knihy pro období ve vašem kalendáři. Doporučujeme spustit proces **Přepočítat období hlavní knihy** v režimu **Dávka** a spustit jej, když se ve vašem systému nevyskytují kritické procesy. V závislosti na počtu transakcí a kombinacích finančních dimenzí může tento proces nějakou dobu trvat.

Pokud u právnické osoby není vybrán žádný fiskální kalendář, při pokusu o zaúčtování transakce v této právnické osobě se zobrazí chybová zpráva.

Více informací získáte v tématu [Fiskální kalendáře, fiskální roky a období](../budgeting/fiscal-calendars-fiscal-years-periods.md).

## <a name="using-a-balancing-financial-dimension"></a>Použití vyrovnávací finanční dimenze

Poté, co vyberete účtovou osnovu a přidáte jednu nebo více účetních struktur, můžete volitelně vybrat jednu finanční dimenzi, která se použije jako vyrovnávací finanční dimenze. Dimenze, kterou vyberete, musí existovat ve všech účetních strukturách. Rovněž musí být vyvážená ve všech účetních položkách. Jinými slovy, částky Má dáti a Dal musí být stejné pro hlavní účet a vyrovnávací finanční dimenzi. Systém automaticky vytváří transakce k vyvážení položek na základě hlavních účtů uvedených v polích **Mezijednotkové účetnictví – částka Dal** a **Mezijednotkové účetnictví – částka Má dáti** na stránce **Účty pro automatické transakce**.

Další informace o vyvažování položek najdete v části [Vyrovnané deníky pro mezijednotkové účetnictví](example-balanced-journals-interunit-accounting.md).

## <a name="configuring-currencies-for-the-ledger"></a>Konfigurace měn pro hlavní knihu

Stránka **Hlavní kniha** se také používá ke kontrole a definování měn, které budou použity při zaúčtování transakcí do hlavní knihy. Musíte určit zúčtovací měnu, což je měna, která se používá ve sloupci **Zúčtovací měna** v hlavní knize ve všech dokladech. Navíc ve sloupci **Měna vykazování** můžete volitelně vybrat druhou měnu. Pokud vyberete měnu vykazování, budou všechny transakce zaznamenány v této měně ve sloupci **Měna vykazování** v hlavní knize na všech dokladech.

Pokud jsou transakce zaúčtovány v jiné měně, systém automaticky převede částku transakce z měny transakcí na zúčtovací měnu a měnu vykazování na dokladu. Na stránce **Hlavní kniha** v poli **Typ směnného kurzu zúčtovací měny** vyberte typ směnného kurzu, který je nakonfigurován pro směnné kurzy, které se mají použít k převodu hodnot z měny transakce na zúčtovací měnu na dokladu. Pokud jste vybrali měnu vykazování, musíte také nastavit pole **Typ směnného kurzu měny vykazování** k zadání směnného kurzu, který se má použít pro převod hodnot z měny transakce na měnu vykazování na dokladu.

Pokud používáte funkci rozpočtování, můžete také nastavit pole **Typ směnného kurzu rozpočtu** k zadání směnného kurzu, který se má použít k převodu rozpočtových transakcí z jedné měny do druhé.

Pokud používáte dvě měny nebo používáte jednu měnu, ale transakce jsou zaúčtovány v jiné měně, musíte nakonfigurovat záložku s náhledem **Účty přecenění měny** na stránce **Hlavní kniha**. Na této záložce s náhledem definujete realizované a nerealizované účty zisků a ztrát, které se ve výchozím nastavení použijí při zaúčtování transakcí, pokud na stránce **Účty přecenění měny** není zadán žádný účet. (Stránka **Účty přecenění měny** slouží ke konfiguraci různých účtů pro realizované a nerealizované zisky a ztráty pro každou měnu.)

Realizované zisky a ztráty jsou zisky a ztráty z dokončených transakcí. Zaznamenávají se do výkazu zisků a ztrát. Nerealizované zisky a ztráty jsou zisky a ztráty, které se uskutečnily, ale transakce není dokončena. Jinými slovy, zaúčtovali jste například fakturu, ale faktura ještě není vyrovnána a zaplacena. Nerealizované zisky a ztráty se zaznamenávají do rozvahy.

Další informace, jak použít dvě měny, naleznete v části [Duální měna](dual-currency.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
