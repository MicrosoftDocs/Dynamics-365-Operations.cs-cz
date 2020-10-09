---
title: Domovská stránka Závazků
description: Toto téma poskytuje přehled závazků.
author: ShylaThompson
manager: AnnBe
ms.date: 02/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21901
ms.assetid: 1e4c2ac4-077b-4678-8733-5cec8f6ff659
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: b663f63552f9de4dbafc0cb71b4381db6d8dc99a
ms.sourcegitcommit: 71a7fb9e7133d872790ec25def5453bbbb17c627
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888149"
---
# <a name="accounts-payable-home-page"></a>Domovská stránka Závazků

[!include [banner](../includes/banner.md)]

Toto téma poskytuje přehled závazků. 

Faktury dodavatele můžete zadat ručně nebo je lze obdržet elektronickou cestou prostřednictvím datové entity. Poté, co jsou faktury zadány nebo přijaty, můžete zkontrolovat a schválit faktury pomocí deníku schválených faktur nebo stránky **Faktura dodavatele**. Můžete použít párování faktur, zásady faktur dodavatele a workflow k automatizaci procesu kontroly tak, aby se automaticky schvalovaly faktury, které splňují určitá kritéria, a zbývající faktury se označily ke kontrole autorizovaným uživatelem.

**Obchodní procesy**

[![Diagram obchodních procesů](./media/AP-process.PNG)](./media/AP-process.PNG)

## <a name="set-up-accounts-payable"></a>Nastavení modulu Závazky

Nastavte skupiny dodavatelů, dodavatele, účetní profily, různé možnosti plateb, parametry týkající se dodavatelů, poplatky, místa expedice a příjmu, vlastní směnky a jiné druhy informací o modulu Závazky. 

[Přehled konfigurace závazků](accounts-payable-overview.md)

[Účetní distribuce a účetní položky dílčí hlavní knihy pro faktury dodavatele](accounting-distributions-subledger-journal-entries-vendor-invoices.md) 

[Přecenění cizí měny pro moduly Závazky a Pohledávky](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md)

## <a name="configure-vendor-invoices"></a>Konfigurace faktur dodavatele

Modul Závazky slouží ke sledování faktur a průběžných výdajů pro dodavatele.

[Přehled párování faktur závazků](accounts-payable-invoice-matching.md)

[Účetní profily dodavatele](vendor-posting-profiles.md)

[Nastavení ověření párování faktur závazků](tasks/set-up-accounts-payable-invoice-matching-validation.md)

[Zásady třícestného párování](three-way-matching-policies.md)

[Párování faktur a mezipodnikové nákupní objednávky](invoice-matching-intercompany-purchase-orders.md)

[Přehled řešení nesrovnalostí během párování součtů faktur](resolve-invoice-totals-invoice-matching-discrepancies.md)

[Výchozí protiúčty pro deníky faktur dodavatele a deníky schvalování faktur](default-offset-accounts-vendor-invoice-journals.md)

[Mobilní schvalování faktur](mobile-invoice-approvals.md)

[Pracovní prostor fakturace dodavatelské spolupráce](vendor-portal-invoicing-workspace.md)

[Automatizace faktur dodavatele](vendor-invoice-automation.md)

## <a name="configure-vendor-payments"></a>Konfigurace plateb dodavatelů 

Přiřaďte typy platby definované systémem, jako je Šek, elektronická platba nebo vlastní směnka k jakékoli uživatelské metodě platby. Typy plateb nejsou povinné, ale jsou užitečné při ověřování elektronických plateb a když potřebujete rychle určit použitý typ platby. 

[Pracovní prostor plateb dodavatelů](vendor-payments-workspace.md)

[Definování platebních poplatků dodavatelů](tasks/define-vendor-payment-fees.md)

[Definování platebních podmínek dodavatelů](tasks/define-vendor-payment-terms.md)

[Přehled platné platby](positive-pay-overview.md)

[Nastavení a generování souborů kladné platby](set-up-generate-positive-pay-files.md)

[Vytvoření plateb dodavatelů pomocí návrhu platby](create-vendor-payments-payment-proposal.md)

[Platby částečných částek dodavatelem](vendor-payments-partial-amount.md)

[Použití slevy, která je větší, než vypočítaná sleva pro platbu dodavatele](take-discount-more-calculated-discount-vendor-payment.md)

[Provedení platební slevy mimo období platební slevy](take-cash-discount-outside-cash-discount-timeframe.md)

[Vzorové šeky dodavatele elektronického výkaznictví](electronic-reporting-sample-vendor-checks.md)

[Stornování platby dodavatele](reverse-vendor-payment.md)

[Zálohové faktury a zálohy](prepayments-invoices-vs-prepayments.md)

[Centralizované platby pro modul Závazky](centralized-payments-accounts-payable.md)

## <a name="settlements"></a>Vyrovnání

Následující témata obsahují informace o vyrovnání. Vyrovnání je proces vyrovnání plateb s fakturami. 

[Konfigurace vyrovnání](../cash-bank-management/configure-settlement.md)

[Vyrovnání částečné platby dodavatele před datem slevy s konečnou platbou po datu slevy](settle-partial-vendor-payment-before-discount-or-final-payment-after.md)

[Vyrovnání částečné platby dodavatele, u níž jsou slevy pro dobropisy dodavatele](settle-partial-vendor-payment-discounts-vendor-credit-notes.md)

[Vyrovnání částečné platby dodavatele, u níž je více období slev](settle-partial-vendor-payment-multiple-discount-periods.md)

[Vyrovnání částečné platby dodavatele a konečné platby před datem slevy](settle-partial-vendor-payment-or-final-payment-before-discount.md)

[Jeden doklad se záznamy několika odběratelů nebo dodavatelů](single-voucher-multiple-customer-vendor-records.md)



### <a name="additional-resources"></a>Další zdroje

#### <a name="whats-new-and-in-development"></a>Co je nového a na čem se pracuje

Přejděte na [plány vydání verzí aplikace Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2010158) a zjistěte, jaké nové funkce se plánují. 

#### <a name="blogs"></a>Blogy

Názory, novinky a jiné informace o závazcích a jiných řešeních naleznete na [blogu Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) a [blogu Microsoft Dynamics 365 Finance - Financials](https://community.dynamics.com/365/financeandoperations/b/financials).

[Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) představuje pro partnery Microsoft Dynamics jediný zdroj informací o tom, co je nového a co se chystá v rámci Dynamics 365.

#### <a name="community-blogs"></a>Blogy komunity

[Správa závazků v Dynamics 365 Finance](https://financefunction.tech/2019/02/15/how-to-manage-payables-in-dynamics-365-for-finance-and-operations)

#### <a name="task-guides"></a>Průvodci záznamem úloh
V aplikaci je k dispozici další nápověda v podobě průvodců záznamem úloh. Průvodce záznamem úloh zobrazíte kliknutím na tlačítko Nápověda na kterékoliv stránce.

#### <a name="videos"></a>Videa

Prohlédněte si instruktážní videa, která jsou nyní k dispozici na [kanálu Microsoft Dynamics 365 YouTube](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).




