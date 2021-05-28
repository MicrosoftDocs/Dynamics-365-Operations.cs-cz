---
title: Změna zúčtovací měny nebo měny vykazování
description: Toto téma vysvětluje, jak změnit zúčtovací měnu nebo měnu vykazování nebo jak přidat měnu vykazování k nastavení hlavní knihy.
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 38b2cdb618d92dca7909a145e7fc07ddfc5f4d45
ms.sourcegitcommit: b67665ed689c55df1a67d1a7840947c3977d600c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6017048"
---
# <a name="change-the-accounting-or-reporting-currency"></a>Změna zúčtovací měny nebo měny vykazování

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak změnit zúčtovací měnu nebo měnu vykazování nebo jak přidat měnu vykazování k nastavení hlavní knihy.

## <a name="symptom"></a>Příznak

Chcete změnit zúčtovací měnu nebo měnu vykazování nebo přidat měnu vykazování k nastavení hlavní knihy. K tomu obvykle dochází v následujících scénářích:

- Při nastavení právnické osoby byla zadána nesprávná zúčtovací měna nebo měna vykazování. Teď chcete tuto měnu změnit.
- Při nastavení právnické osoby nebyla zadána žádná měna vykazování. (Měna vykazování je volitelná.) Teď chcete měnu vykazování přidat.

Organizace, která dříve funkci duální měny nevyužívala, ji chce začít používat. K tomuto problému obvykle dochází v následujících scénářích:

- Měna vykazování byla při založení právnické osoby zadána, ale organizace teď chce měnu vykazování odebrat.
- Organizace upgraduje nebo migruje na Microsoft Dynamics 365 Finance a chce změnit zúčtovací měnu nebo měnu vykazování.

## <a name="resolution"></a>Řešení

Nejdůležitější je zjistit, zda byly nějaké transakce (skutečné nebo rozpočtové) právnické osoby pro nastavení hlavní knihy zaúčtovány. **Pokud v právnické osobě byly nějaké transakce (skutečné nebo rozpočtové) zaúčtovány, nemůžete zúčtovací měnu nebo měnu vykazování změnit ani měnu vykazování přidat.** Podle toho, zda byly transakce zaúčtovány, postupujte podle kroků v jedné z následujících částí.

### <a name="no-transactions-have-been-posted"></a>Nebyly zaúčtovány žádné transakce

1. V právnické osobě, pro kterou měny aktualizujete, přejděte k nabídce **Hlavní kniha \> Nastavení hlavní knihy \> Hlavní kniha**.
2. Na stránce **Hlavní kniha** vyberte možnost **Upravit**.
3. Na záložce s náhledem **Měna** vyberte zúčtovací měnu a měnu vykazování, které se mají pro právnickou osobu použít.
4. Zvolte možnost **Uložit**.

Pokud nejsou pole pro zúčtovací měnu a měnu vykazování na stránce **Hlavní kniha** k dispozici, byla v právnické osobě zaúčtována jedna nebo více transakcí (skutečných nebo rozpočtových). Měny proto nejde změnit. V takovém případě postupujte podle kroků v další části.

### <a name="transactions-have-been-posted"></a>Transakce byly zaúčtovány

**Pokud byly v právnické osobě zaúčtovány transakce, jediným způsobem, jak změnit nebo přidat zúčtovací měnu a měnu vykazování, je vytvoření nové právnické osoby, která má správné měny.** K usnadnění tohoto procesu umožňuje Správa dat kopírovat v systému záznamy o nastavení a hlavní záznamy z aktuální právnické osoby do nové právnické osoby.

Změny v zúčtovací měně a měně vykazování mají dopad na vše. Ovlivňují nejen hlavní knihu, ale také všechny dílčí hlavní knihy (pohledávky, závazky, zásoby, projekt atd.), všechna řešení nezávislých dodavatelů softwaru (ISV) a jakékoli rozšíření, které jste vytvořili a které ukládá částky.

Proces hledání a převodu jednotlivých částek do jiné měny podléhá chybám. Vývojový tým proto neschválí skript, který mění nebo přidává zúčtovací měny a měnu vykazování. Přestože vám navíc nástroj, který byl k dispozici pro Microsoft Dynamics AX 2012, umožňuje zúčtovací měnu a měnu vykazování měnit nebo přidávat, tento nástroj je již pro AX 2012 R3 i Finance zastaralý.

Pomocí těchto kroků zkopírujte nastavení a hlavní data z aktuální právnické osoby do nové právnické osoby.

1. Přejděte k nabídce **Pracovní prostory \> Správa dat**.
2. Vyberte možnost **Šablony** ve skupině **Import/export**.
3. Zkontrolujte, zda jsou šablony k dispozici. Pokud nejsou k dispozici žádné šablony, vyberte možnost **Načíst výchozí šablony** a počkejte na vygenerování šablon.
4. Přejděte zpět k pracovnímu prostoru **Správa dat**.
5. Vyberte možnost **Kopírování do právnické osoby**.
6. Zadejte název a popis skupiny.
7. V poli **Zdrojová právnická osoba** vyberte právnickou osobu, ze které chcete kopírovat data.
8. Na záložce s náhledem **Cílové právnické osoby** vytvořte výběrem možnosti **Vytvořit právnické osoby** novou právnickou osobu, do které můžete zkopírovat data zdrojové právnické osoby. Ke zkopírování dat do existující právnické osoby vyberte možnost **Vybrat existující**.
9. Volitelné: Nastavte pole **Kopírovat číselné řady** na hodnotu **Ano**. (Tento krok se doporučuje při kopírování dat.)
10. V oblasti **Vybrané entity** vyberte možnost **Přidat šablonu**.
11. Vyberte, které šablony se použijí. Navrhované šablony pro novou právnickou osobu zahrnují **025 - Hlavní kniha** a **Finance**. Doporučujeme vám zkontrolovat všechny ostatní dostupné šablony, abyste zjistili, zda by šly některé použít pro vaše požadavky.
12. Výběrem možnosti **Kopírování do právnické osoby** spusťte dávkové zpracování, které vytvoří vybrané entity a zkopíruje je do cílové právnické osoby.
13. Po dokončení procesu, ale před zaúčtováním jakékoli transakce, přejděte do hlavní knihy a aktualizujte zúčtovací měnu a měnu vykazování, jak je popsáno výše v tomto tématu.

Pokud jste vytvořili novou právnickou osobu, abyste mohli zúčtovací měnu nebo měnu vykazování změnit, ověřte, zda jsou počáteční zůstatky převedeny z měn staré právnické osoby na nové měny.

Video, které zobrazuje předchozí kroky, najdete v části [Kopírování do právnické osoby](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).
