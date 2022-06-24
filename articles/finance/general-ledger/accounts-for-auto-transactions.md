---
title: Účty pro automatické transakce
description: Tento článek vysvětluje, jak se účty pro automatické transakce používají k zaúčtování přes Microsoft Dynamics 365 a poskytuje příklady klíčových účtů pro automatické transakce.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74e72840fea1f5d89c908b00e2cf572bce6befbe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880752"
---
# <a name="accounts-for-automatic-transactions"></a>Účty pro automatické transakce

Stránka **Účty pro automatické transakce** (**Hlavní kniha &gt; Nastavení zaúčtování &gt; Účty pro automatické transakce**) se používá k definování výchozího hlavního účtu, který se používá pro jednotlivé typy účtování v systému. Přestože většinu typů účtování lze konfigurovat na stránce specifické pro modul nebo funkci, některé typy účtování lze konfigurovat pouze na stránce **Účty pro automatické transakce**.

Můžete například zadat hlavní účet, který se používá pro typ účtování **Zůstatek zákazníků** v poli **Souhrn** na stránce **Profil účtování zákazníka** a pro každý profil zákazníka použít jiný hlavní účet. Tímto způsobem máte podrobnější kontrolu nad účtováním. Na druhé straně můžete specifikovat účet chyby pouze na stránce **Účty pro automatické transakce**.

Když otevřete stránku **Účty pro automatické transakce** v nové právnické osobě, bude seznam účtů prázdný. Výběrem možnosti můžete přidat nejběžnější typy příspěvků, které by měly být na stránce konfigurovány, výběrem tlačítka **Vytvořit výchozí typy**. Poté můžete pro každý řádek vybrat hlavní účet v poli **Hlavní účet**. Pokud pole **Hlavní účet** necháte prázdné pro typ účtování a nenakonfigurovali jste hlavní účet na stránce specifické pro modul nebo funkci, obdržíte chybovou zprávu, když zaúčtujete transakci, která používá typ účtování. Obvykle bude zpráva vypadat následovně: „Účet pro \[Typ účtování\] nelze najít.“

## <a name="default-posting-types"></a>Výchozí typy účtování

Následující tabulka ukazuje příklady výchozích typů účtování, které se vytvoří, když vyberete **Vytvořit výchozí typy** na stránce **Účty pro automatické transakce**. Zobrazuje ukázkové hlavní účty a popisy. Sloupec „Debetní/kreditní?“ udává, zda transakce obvykle zahrnuje debet nebo kredit. V některých případech může transakce zaúčtovat buď debet, nebo kredit. Sloupec „Clearingový“ účet označuje, zda typ účtování je clearingový účet. Pokud je typ účtování clearingový účet, částka zaúčtovaná na tomto účtu je automaticky stornována při zaúčtování pozdější transakce.

| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | Popis |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Haléřový rozdíl v měně vykazování | 618160 | Vedlejší výdaje | Výdaje | Oboje | Ne | Tento typ účtování se používá, když dojde k haléřovému rozdílu, když se částka transakce v cizí měně převede do měny vykazování. |
| Haléřový rozdíl v zúčtovací měně | 618160 | Vedlejší výdaje | Výdaje | Oboje | Ne | Tento typ účtování se používá, když dojde k haléřovému rozdílu, když se částka transakce v cizí měně převede do účetní měny. |
| Chybový účet | 999999 | Chybový účet | Výdaje | Oboje | Ne | Tento typ účtování se používá, když v systému dojde k chybě. Účet by měl být ověřován každé období a měly by být vyřešeny všechny chyby. |
| Roční uzávěrka | 300160 | Pozdržené příjmy | Jmění | Oboje | Ne | Tento typ účtování se používá, když je spuštěn proces uzavření na konci roku k přesunutí zůstatku účtů typů **Zisk a ztráta** do hlavního účtu, který je vybrán pro výsledek na konci roku. |
| Platební sleva odběratele | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ne | Typ účtování, který je definován na stránce **Účty pro automatické transakce**, se nepoužívá. Hlavní účet je vyžadován, když jsou hotovostní slevy nakonfigurovány v části Pohledávky.|
| Platební sleva dodavatele | Nelze použít | Nelze použít | Nelze použít | Nelze použít | Ne | Typ účtování, který je definován na stránce **Účty pro automatické transakce**, se nepoužívá. Hlavní účet je vyžadován, když jsou hotovostní slevy nakonfigurovány v části Závazky. |

## <a name="additional-posting-types"></a>Další typy účtování

Následující tabulka ukazuje příklady dalších typů účtování, které je nutné nakonfigurovat, pokud plánujete používat související funkce. Pro tyto typy účtování není v jiném modulu k dispozici žádná konfigurace profilu účtování. Sloupec „Debetní/kreditní?“ udává, zda transakce obvykle zahrnuje debet nebo kredit. V některých případech může transakce zaúčtovat buď debet, nebo kredit. Sloupec „Clearingový“ účet označuje, zda typ účtování je clearingový účet. Pokud je typ účtování clearingový účet, částka zaúčtovaná na tomto účtu je automaticky stornována při zaúčtování pozdější transakce.

| Typ zaúčtování | Příklad hlavního účtu | Příklad názvu hlavního účtu | Typ účtu | Debetní/kreditní? | Clearingový účet | Popis |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Rozvahový účet pro konsolidační rozdíl | 801200 | Zisk a ztráta – přecenění | Výdaje | Oboje | Ne | Tento typ účtování se používá, když provádíte konsolidaci, která zahrnuje přecenění měny a během přecenění dochází k haléřovým rozdílům. |
| Účet zisků a ztrát pro konsolidační rozdíly | 801200 | Zisk a ztráta – přecenění | Výdaje | Oboje | Ne | Tento typ účtování se používá, když provádíte konsolidaci, která zahrnuje přecenění měny a během přecenění dochází k haléřovým rozdílům. |
| Mezijednotkové účetnictví – částka Má dáti | 133500 | Mezijednotková pohledávka | Materiál | Debet | Ne | Tento typ účtování se používá, když vyberete vyvažovací dimenzi na stránce **Hlavní kniha** a dimenze se nevyrovnává v transakci, která je zaúčtována. |
| Mezijednotkové účetnictví – částka Dal | 233500 | Mezijednotké závazky | Pasiva | Kredit | Ne | Tento typ účtování se používá, když vyberete vyvažovací dimenzi na stránce **Hlavní kniha** a dimenze se nevyrovnává v transakci, která je zaúčtována. |
