---
title: Migrace potenciálního zákazníka na hotovostní data ze služby Data Integrator do duálního zápisu
description: Tento článek popisuje, jak migrovat potenciálního zákazníka na hotovostní data ze služby Data Integrator do duálního zápisu.
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: 91cc0e59405bc085e09f01f05ef02e4a0260481e
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111887"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Migrace potenciálního zákazníka na hotovostní data ze služby Data Integrator do duálního zápisu

[!include [banner](../../includes/banner.md)]

Řešení Zpeněžení potenciálního zákazníka dostupné pro Integrátor dat není kompatibilní s duálním zápisem. Důvodem je index msdynce_AccountNumber v tabulce účtů, který byl součástí řešení Zpeněžení potenciálního zákazníka. Pokud tento index existuje, nemůžete vytvořit stejné číslo zákaznického účtu ve dvou různých právnických osobách. Můžete buď začít znovu s duálním zápisem migrací dat Zpeněžení potenciálního zákazníka na hotovostní data z Integrátoru dat na duální zápis, nebo můžete nainstalovat poslední „dorman“ verzi řešení Zpeněžení potenciálního zákazníka. Tento článek popisuje oba tyto scénáře.

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>Nainstalujte poslední „dorman“ verzi řešení Integrátor dat - Zpeněžení potenciálního zákazníka

Za poslední „dorman“ verzi řešení Integrátor dat - Zpeněžení potenciálního zákazníka je považována verze **P2C 15.0.0.2**. Můžete si ji stáhnout z webu [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C).

Musíte ji nainstalovat ručně. Po instalaci zůstává vše úplně stejné, kromě toho, že je odstraněn index msdynce_AccountNumber.

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Kroky při migraci dat řešení Zpeněžení ze služby Integrátor dat na duální zápis

Pokud chcete migrovat potenciálního zákazníka na hotovostní data ze služby Data Integrator do duálního zápisu, postupujte následovně.

1. Spusťte program Potenciální zákazník na úlohy integrátoru dat a proveďte jednu konečnou úplnou synchronizaci. Tímto způsobem zajistíte, aby oba systémy (finanční a provozní aplikace a aplikace Customer Engagement) měly všechna data.
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
5. Vytvořte spojení s duálním zápisem mezi finanční a provozní aplikací a aplikací Customer Engagement pro jednu nebo více právnických osob.
6. Povolte mapy tabulek s duálním zápisem a spusťte počáteční synchronizaci pro požadovaná referenční data. (Další informace viz [Úvahy o počáteční synchronizaci](initial-sync-guidance.md).) Příklady požadovaných údajů zahrnují skupiny zákazníků, platební podmínky a platební plány. Nepovolujte mapy duálního zápisu pro tabulky, které vyžadují inicializaci, jako je například účet, nabídka, řádek nabídky, objednávka a tabulky řádků objednávky.
7. V aplikaci Customer Engagement přejděte na **Pokročilé nastavení \> Nastavení systému \> správa dat \> Pravidla pro detekci duplicit** a zakažte všechna pravidla.
8. Inicializujte tabulky uvedené v kroku 2. Pokyny najdete ve zbývajících částech tohoto článku.
9. Otevřete finanční a provozní aplikaci a povolte mapy tabulek, jako je účet, nabídka, řádek nabídky, objednávka a mapy tabulky řádků objednávky. Pak spusťte počáteční synchronizaci. (Další informace viz [Úvahy o počáteční synchronizaci](initial-sync-guidance.md).) Tento proces bude synchronizovat další informace z finanční a provozní aplikace, jako je stav zpracování, dodací a fakturační adresy, weby a sklady.

## <a name="account-table"></a>Tabulka účtu

1. Ve sloupci **Společnost** zadejte název společnosti jako **USMF**.
2. Ve sloupci **Typ vztahu** zadejte jako statickou hodnotu **Zákazník**. Možná nebudete chtít ve své obchodní logice klasifikovat každý záznam účtu jako zákazníka.
3. Ve sloupci **ID skupiny zákazníků** zadejte číslo skupiny zákazníků z finanční a provozní aplikace. Výchozí hodnota z řešení Zpeněžení potenciálního zákazníka je **10**.
4. Pokud používáte řešení Zpeněžení potenciálního zákazníka bez jakéhokoli přizpůsobení **Čísla účtu**, zadejte hodnotu **Číslo účtu** do sloupce **Číslo strany**. Pokud existují přizpůsobení a neznáte číslo strany, vytáhněte tyto informace z finanční a provozní aplikace.

## <a name="contact-table"></a>Kontaktní tabulka

1. Ve sloupci **Společnost** zadejte název společnosti jako **USMF**.
2. Nastavte následující sloupce na základě hodnoty **IsActiveCustomer** v souboru CSV:

    - Pokud je volba **IsActiveCustomer** nastaven na **Ano** v souboru CSV, nastavte sloupec **Prodejný** na **Ano**. Ve sloupci **ID skupiny zákazníků** zadejte číslo skupiny zákazníků z finanční a provozní aplikace. Výchozí hodnota z řešení Zpeněžení potenciálního zákazníka je **10**.
    - Pokud je **IsActiveCustomer** nastaven na **Ne** v souboru CSV, nastavte sloupec **Prodejný** na **Ne** a pak nastavte sloupec **Kontakt pro** na **Zákazník**.

3. Pokud používáte řešení Zpeněžení potenciálního zákazníka bez jakéhokoli přizpůsobení **Kontaktního čísla**, nastavte následující sloupce:

    - Migrujte kontaktní číslo ze souboru CSV (**msdynce\_contactnumber**) na kontaktní číslo v tabulce **Kontakt** (**msdyn\_contactnumber**).
    - Použijte hodnoty z tabulky **Kontaktní číslo** ve sloupci **Číslo strany**.
    - Použijte hodnoty z tabulky **Kontaktní číslo** ve sloupci **Číslo účtu / ID kontaktní osoby**.

## <a name="invoice-table"></a>Tabulka faktury

Protože data z tabulky **Faktura** jsou navržena tak, aby plynula jedním směrem, z finanční a provozní aplikace do aplikace Customer Engagement, inicializace není nutná. Spusťte počáteční synchronizaci a migrujte všechna požadovaná data z finanční a provozní aplikace pro interakci se zákazníkem. Další informace viz [Úvahy o počáteční synchronizaci](initial-sync-guidance.md).

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

Protože data z tabulky **Produkty** jsou navržena tak, aby plynula jedním směrem, z finanční a provozní aplikace do aplikace Customer Engagement, inicializace není nutná. Spusťte počáteční synchronizaci a migrujte všechna požadovaná data z finanční a provozní aplikace pro interakci se zákazníkem. Další informace viz [Úvahy o počáteční synchronizaci](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Nabídka a tabulky produktu Nabídka

Pro tabulku **Nabídka** postupujte podle pokynů v části [Tabulka objednávky](#order-table) dříve v tomto článku. Pro tabulku **Produkt nabídky** postupujte podle pokynů v části [Tabulka produktů objednávky](#order-products-table) dříve v tomto tématu.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

