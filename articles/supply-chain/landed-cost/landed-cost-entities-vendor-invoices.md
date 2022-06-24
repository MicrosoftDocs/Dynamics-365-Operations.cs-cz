---
title: Entity faktur dodavatele
description: Tento článek poskytuje informace o entitách faktur dodavatele, které umožňují konfigurovat kódy typů nákladů pro interní náklady nebo externě odvozené náklady.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 171b383e1549babd76fd18e4932436a66aa62cc1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873920"
---
# <a name="vendor-invoice-entities"></a>Entity faktury dodavatele

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Modul **Náklady za doručení** umožňuje konfigurovat kódy typu nákladů pro interní náklady nebo externě odvozené náklady. Pokud jde o náklady mimo podnik, očekává se od poskytovatele služeb faktura. Tato faktura je zpracována jako deník faktur, který lze přiřadit k cestě, a hodnotu faktury lze rozdělit na jeden nebo více nákladů na cestu.

Entity faktury dodavatele umožňují přidělení hodnoty řádku deníku mezi jeden nebo více nákladů na cestu, které sdílejí stejný kód typu nákladů.

Náklady lze přiřadit pouze v případě, že existuje záhlaví deníku faktur a řádky deníku faktur.

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>Přidělení nákladů na cestu dodavatele (ITMLedgerJournalCostLinesVoyagesEntity)

Datová entita přidělení nákladů na cestu dodavatele umožňuje přidělit řádek faktury dodavatele mezi jeden nebo více nákladů, které jsou aplikovány na oblast nákladů na cestu. Tato funkce je podporována entitou `ITMLedgerJournalCostLinesVoyagesEntity`. Následující tabulka uvádí pole a mapování, které tvoří tuto entitu.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Přidělená částka | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Číslo | Číslo |
| Číslo řádku nákladové transakce | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ano** | Číslo |
| Číslo řádku deníku | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ano** | Číslo |
| Číslo deníku | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ano** | Číslo |
| Cesta | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ano** | Číslo |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>Přidělení nákladů na přepravní kontejnery dodavatele (ITMLedgerJournalCostLinesContainersEntity)

Datová entita přidělení nákladů na přepravní kontejner dodavatele umožňuje přidělit řádek faktury dodavatele mezi jeden nebo více nákladů, které jsou aplikovány na oblast nákladů na přepravní kontejner. Tato funkce je podporována entitou `ITMLedgerJournalCostLinesContainersEntity`. Následující tabulka uvádí pole a mapování, které tvoří tuto entitu.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Přidělená částka | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Číslo | Číslo |
| Přepravní kontejner | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ano** | Číslo |
| Číslo řádku nákladové transakce | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ano** | Číslo |
| Číslo řádku deníku | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ano** | Číslo |
| Číslo deníku | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ano** | Číslo |
| Cesta | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ano** | Číslo |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>Přidělení nákladů na folio dodavatele (ITMLedgerJournalCostLinesFoliosEntity)

Datová entita přidělení nákladů na folio dodavatele umožňuje přidělit řádek faktury dodavatele mezi jeden nebo více nákladů, které jsou aplikovány na oblast nákladů folia. Tato funkce je podporována entitou `ITMLedgerJournalCostLinesFoliosEntity`. Následující tabulka uvádí pole a mapování, které tvoří tuto entitu.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Přidělená částka | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Číslo | Číslo |
| Číslo řádku nákladové transakce | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ano** | Číslo |
| Folio | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ano** | Číslo |
| Číslo řádku deníku | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ano** | Číslo |
| Číslo deníku | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ano** | Číslo |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>Přidělení nákladů nákupní objednávky dodavatele (ITMLedgerJournalCostLinesPurchTableEntity)

Datová entita přidělení nákladů nákupní objednávky dodavatele umožňuje přidělit řádek faktury dodavatele mezi jeden nebo více nákladů, které jsou aplikovány na oblast nákladů nákupní objednávky. Tato funkce je podporována entitou `ITMLedgerJournalCostLinesPurchTableEntity`. Následující tabulka uvádí pole a mapování, které tvoří tuto entitu.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Přidělená částka | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Číslo | Číslo |
| Číslo řádku nákladové transakce | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ano** | Číslo |
| Číslo řádku deníku | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ano** | Číslo |
| Číslo deníku | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ano** | Číslo |
| Nákupní objednávka | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ano** | Číslo |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>Přidělení nákladů položky dodavatele (ITMLedgerJournalCostLinesPurchLineEntity)

Datová entita přidělení nákladů na položku dodavatele umožňuje přidělit řádek faktury dodavatele mezi jeden nebo více nákladů, které jsou aplikovány na oblast nákladů položky. Oblast nákladů položky pokrývá náklady na řádku nákupní objednávky. Tato funkce je podporována entitou `ITMLedgerJournalCostLinesPurchLineEntity`. Následující tabulka uvádí pole a mapování, které tvoří tuto entitu.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Přidělená částka | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Číslo | Číslo |
| Číslo řádku nákladové transakce | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ano** | Číslo |
| Číslo řádku deníku | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ano** | Číslo |
| Číslo deníku | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ano** | Číslo |
| Nákupní objednávka | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ano** | Číslo |
| Číslo řádku nákupní objednávky | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ano** | Číslo |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>Přidělení nákladů na řádek převodního příkazu dodavatele (ITMLedgerJournalCostLinesTransferLineEntity)

Datová entita přidělení nákladů na řádek převodního příkazu dodavatele umožňuje přidělit řádek faktury dodavatele mezi jeden nebo více nákladů, které jsou aplikovány na oblast nákladů řádku převodu. Tato funkce je podporována entitou `ITMLedgerJournalCostLinesTransferLineEntity`. Následující tabulka uvádí pole a mapování, které tvoří tuto entitu.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Přidělená částka | ITMLedgerJournalCostLines.Amount | Numeric(32, 6) | Číslo | Číslo |
| Číslo řádku nákladové transakce | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ano** | Číslo |
| Číslo řádku deníku | ITMLedgerJournalCostLines.RefRecId | Numeric(32, 16) | **Ano** | Číslo |
| Číslo deníku | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Ano** | Číslo |
| Převodní příkaz | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Ano** | Číslo |
| Číslo řádku převodního příkazu | ITMLedgerJournalCostLines.CostTransRefRecId | Numeric(32, 16) | **Ano** | Číslo |

### <a name="reference-table"></a>Referenční tabulka

Nákladové řádky cesty mají přímou souvislost se záznamem nákladové transakce. Tento záznam zahrnuje **ID referenční tabulky**. Tato hodnota je jedinečná u každé nákladové oblasti (cesta, přepravní kontejner atd.). Když se u dat vytvořených pomocí datových entit odkazuje na konkrétní čísla tabulek, entity se rozdělí na základě hodnot **ID referenční tabulky**.

Hodnoty pro referenční tabulku (`RefTableId`) a typ transakce (`TransType`) jsou implicitní ve výběru entity nákupního řádku nákladů za doručení nebo entity řádku převodu nákladů za doručení.

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>Řádky deníku faktury dodavatele (VendorInvoiceJournalLineEntity)

Než lze hodnotu řádku deníku přiřadit k jednomu nebo více nákladům v modulu **Náklady za doručení**, řádek deníku musí být spojen s nákladovou oblastí. Modul **Náklady za doručení** přidává některá nová pole do tabulky řádků deníku (`LedgerJournalTrans`), aby se tato funkčnost dala používat.

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>Pole přidaná do entity řádku deníku faktur dodavatele

V následující tabulce jsou uvedena pole, která modul **Náklady za doručení** přidá do entity řádku deníku faktur dodavatele (`VendorInvoiceJournalLineEntity`). Tato pole umožňují systému vytvářet řádky deníku a přiřazovat jim náklady.

| Jméno | Mapování | Datový typ | Klíč | Povinné |
|---|---|---|---|---|
| Nákladová oblast | LedgerJournalTrans.ITMCostArea | Int | Číslo | Číslo |
| Kód typu nákladů | LedgerJournalTrans.ITMCostTypeId | Nvarchar(20) | Číslo | Číslo |

### <a name="mainoffset-account"></a>Hlavní účet/protiúčet

Hlavní účet / protiúčet pro řádek deníku faktury, který je spojen s náklady za doručení cesty, je určen kódem typu nákladů. Když je kód typu nákladů zahrnut do řádku deníku faktur, bude zúčtovací účet pro kód použit buď jako hlavní účet, nebo jako protiúčet, v závislosti na scénáři:

- **Jednořádkový deník** – Pokud je definován hlavní účet (jinými slovy účet dodavatele) a je uveden kód typu nákladů, hodnota zúčtovacího účtu pro tento kód druhu nákladů bude vložena do protiúčtu.
- **Víceřádkový deník** – Pokud hlavní účet není definován, ale je uveden kód typu nákladů, hodnota zúčtovacího účtu pro tento kód druhu nákladů bude vložena do hlavního účtu. Řádek deníku, který připisuje dodavateli, nebude odkazovat na kód typu nákladů.

## <a name="sequencing"></a>Klasifikace

Kvůli závislostem mezi deníkem a tabulkami řádků deníku musí být nejprve vytvořen záznam o cestě. Řádky cesty lze vytvořit až po vytvoření cesty, přepravního kontejneru a folií.

Pro přidělení faktury za cestu musí systém zpracovat entity v následujícím pořadí:

1. Záhlaví deníku faktur (`VendInvoiceJournalHeaderEntity`)
1. Řádek deníku faktur (`VendInvoiceJournalLineEntity`)
1. Přidělení nákladů za doručení (`ITMLedgerJournalEntities`)
