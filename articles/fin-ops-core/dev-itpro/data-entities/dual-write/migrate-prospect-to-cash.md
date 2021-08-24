---
title: Migrace potenciálního zákazníka na hotovostní data ze služby Data Integrator do duálního zápisu
description: Toto téma popisuje, jak migrovat potenciálního zákazníka na hotovostní data ze služby Data Integrator do duálního zápisu.
author: RamaKrishnamoorthy
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-01-04
ms.openlocfilehash: 46f869265e589ad8e0c94a839df70e54fe781c5a4e7f992e6534e883b21801ae
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733116"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Migrace potenciálního zákazníka na hotovostní data ze služby Data Integrator do duálního zápisu

[!include [banner](../../includes/banner.md)]

Pokud chcete migrovat potenciálního zákazníka na hotovostní data ze služby Data Integrator do duálního zápisu, postupujte následovně.

1. Spusťte program Potenciální zákazník na úlohy integrátoru dat a proveďte jednu konečnou úplnou synchronizaci. Tímto způsobem zajistíte, aby oba systémy (aplikace Finance and Operations a aplikace Customer Engagement) měly všechna data.
2. Chcete-li zabránit možné ztrátě dat, exportujte data Potenciální zákazník pro hotovost z Microsoft Dynamics 365 Sales do souboru Excel nebo do souboru hodnot oddělených čárkami (CSV). Exportujte data z následujících entit:

    - [Účet](#account-table)
    - [Kontakt](#contact-table)
    - [Faktura](#invoice-table)
    - Fakturační produkty
    - [Objednat](#order-table)
    - [Objednání produktů](#order-products-table)
    - [Produkty](#products-table)
    - [Nabídka](#quote-and-quote-product-tables)
    - [Nabídka produktů](#quote-and-quote-product-tables)

3. Odinstalujte řešení Potenciální zákazník pro hotovost z prodejního prostředí. Tento krok odstraní sloupce a odpovídající data, která zavedlo řešení Potenciální zákazník pro hotovost.
4. Nainstalujte řešení pro duální zápis.
5. Vytvořte spojení s duálním zápisem mezi aplikací Finance and Operations a aplikací Customer Engagement pro jednu nebo více právnických osob.
6. Povolte mapy tabulek s duálním zápisem a spusťte počáteční synchronizaci pro požadovaná referenční data. (Další informace viz [Úvahy o počáteční synchronizaci](initial-sync-guidance.md).) Příklady požadovaných údajů zahrnují skupiny zákazníků, platební podmínky a platební plány. Nepovolujte mapy duálního zápisu pro tabulky, které vyžadují inicializaci, jako je například účet, nabídka, řádek nabídky, objednávka a tabulky řádků objednávky.
7. V aplikaci Customer Engagement přejděte na **Pokročilé nastavení \> Nastavení systému \> správa dat \> Pravidla pro detekci duplicit** a zakažte všechna pravidla.
8. Inicializujte tabulky uvedené v kroku 2. Pokyny najdete ve zbývajících částech tohoto tématu.
9. Otevřete aplikaci Finance and Operations a povolte mapy tabulek, jako je účet, nabídka, řádek nabídky, objednávka a mapy tabulky řádků objednávky. Pak spusťte počáteční synchronizaci. (Další informace viz [Úvahy o počáteční synchronizaci](initial-sync-guidance.md).) Tento proces bude synchronizovat další informace z aplikace Finance and Operations, jako je stav zpracování, dodací a fakturační adresy, weby a sklady.

## <a name="account-table"></a>Tabulka účtu

1. Ve sloupci **Společnost** zadejte název společnosti jako **USMF**.
2. Ve sloupci **Typ vztahu** zadejte jako statickou hodnotu **Zákazník**. Možná nebudete chtít ve své obchodní logice klasifikovat každý záznam účtu jako zákazníka.
3. Ve sloupci **ID skupiny zákazníků** zadejte číslo skupiny zákazníků z aplikace Finance and Operations. Výchozí hodnota z řešení Zpeněžení potenciálního zákazníka je **10**.
4. Pokud používáte řešení Zpeněžení potenciálního zákazníka bez jakéhokoli přizpůsobení **Čísla účtu**, zadejte hodnotu **Číslo účtu** do sloupce **Číslo strany**. Pokud existují přizpůsobení a neznáte číslo strany, vytáhněte tyto informace z aplikace Finance and Operations.

## <a name="contact-table"></a>Kontaktní tabulka

1. Ve sloupci **Společnost** zadejte název společnosti jako **USMF**.
2. Nastavte následující sloupce na základě hodnoty **IsActiveCustomer** v souboru CSV:

    - Pokud je volba **IsActiveCustomer** nastaven na **Ano** v souboru CSV, nastavte sloupec **Prodejný** na **Ano**. Ve sloupci **ID skupiny zákazníků** zadejte číslo skupiny zákazníků z aplikace Finance and Operations. Výchozí hodnota z řešení Zpeněžení potenciálního zákazníka je **10**.
    - Pokud je **IsActiveCustomer** nastaven na **Ne** v souboru CSV, nastavte sloupec **Prodejný** na **Ne** a pak nastavte sloupec **Kontakt pro** na **Zákazník**.

3. Pokud používáte řešení Zpeněžení potenciálního zákazníka bez jakéhokoli přizpůsobení **Kontaktního čísla**, nastavte následující sloupce:

    - Migrujte kontaktní číslo ze souboru CSV (**msdynce\_contactnumber**) na kontaktní číslo v tabulce **Kontakt** (**msdyn\_contactnumber**).
    - Použijte hodnoty z tabulky **Kontaktní číslo** ve sloupci **Číslo strany**.
    - Použijte hodnoty z tabulky **Kontaktní číslo** ve sloupci **Číslo účtu / ID kontaktní osoby**.

## <a name="invoice-table"></a>Tabulka faktury

Protože data z tabulky **Faktura** jsou navržena tak, aby plynula jedním směrem, z aplikace Finance and Operations do aplikace Customer Engagement, inicializace není nutná. Spusťte počáteční synchronizaci a migrujte všechna požadovaná data z aplikace Finance and Operations pro interakci se zákazníkem. Další informace viz [Úvahy o počáteční synchronizaci](initial-sync-guidance.md).

## <a name="order-table"></a>Tabulka objednávek

1. Ve sloupci **Společnost** zadejte název společnosti jako **USMF**.
2. Zkopírujte hodnotu sloupce **ID objednávky** v souboru CSV do sloupce **Číslo prodejní objednávky**.
3. Zkopírujte hodnotu sloupce **Zákazník** v souboru CSV do sloupce **Číslo zákazníka faktury**.
4. Zkopírujte hodnotu sloupce **Země/oblast dodání** v souboru CSV do sloupce **Země/oblast dodání**. Mezi příklady této hodnoty patří **USA** a **Spojené státy**.
5. Nastavte sloupec **Požadované datum přijetí**. Pokud nepoužíváte datum přijetí, použijte sloupce **Požadované datum dodávky**, **Datum splnění** a **Datum odeslání** v souboru CSV. Příkladem této hodnoty je **2020-03-27T00: 00: 00Z**.
6. Nastavte sloupec **Jazyk**. Příkladem této hodnoty je **en-us**.
7. Nastavte sloupec **Typ objednávky** pomocí sloupce **Na základě položky**.

## <a name="order-products-table"></a>Objednat tabulku produktů

- Ve sloupci **Společnost** zadejte název společnosti jako **USMF**.

## <a name="products-table"></a>Tabulka produktů

Protože data z tabulky **Produkty** jsou navržena tak, aby plynula jedním směrem, z aplikace Finance and Operations do aplikace Customer Engagement, inicializace není nutná. Spusťte počáteční synchronizaci a migrujte všechna požadovaná data z aplikace Finance and Operations pro interakci se zákazníkem. Další informace viz [Úvahy o počáteční synchronizaci](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Nabídka a tabulky produktu Nabídka

Pro tabulku **Nabídka** postupujte podle pokynů v části [Tabulka objednávky](#order-table) dříve v tomto tématu. Pro tabulku **Produkt nabídky** postupujte podle pokynů v části [Tabulka produktů objednávky](#order-products-table) dříve v tomto tématu.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]