---
title: Řešení problémů s prodejními objednávkami
description: Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s prodejními objednávkami.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 8f4a28b0cf47ec1c2534fc97c4dee6790fa6c51637bddf64caa7147e9ce6d6db
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746105"
---
# <a name="troubleshoot-sales-orders"></a>Řešení problémů s prodejními objednávkami

Toto téma popisuje, jak vyřešit problémy, s nimiž se můžete setkat při práci s prodejními objednávkami.

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a>Daňové informace se neaktualizují, pokud změním umístění v záhlaví prodejní objednávky.

### <a name="issue-description"></a>Popis problému

Pokud se pracoviště, sklad nebo adresa dodání změní buď v záhlaví prodejní objednávky, nebo na úrovni řádku, informace o dani případu se pro řádky automaticky neaktualizují.

### <a name="issue-resolution"></a>Řešení problému

Toto chování je záměrné. K problému dochází, protože ani doručovací adresa, pracoviště a sklad se na úrovni řádku automaticky nezmění. Musíte je aktualizovat ručně.

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a>Pokud existují dvě obchodní smlouvy pro stejné období nebo překrývající se období, je vždy vybrán stejný řádek smlouvy.

### <a name="issue-description"></a>Popis problému

Pokud jsou definovány dvě obchodní smlouvy pro stejné období nebo překrývající se období, zdá se, že stejná obchodní smlouva je vybrána pokaždé, když vytvoříte řádky prodejní objednávky, které obsahují tyto položky.

### <a name="issue-resolution"></a>Řešení problému

Pokud pro dané datum existuje více než jedna obchodní smlouva, je vždy vybrána obchodní smlouva, která má nejnižší cenu. Další informace získáte stažením následujícího dokumentu whitepaper: [Obchodní smlouvy v Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>Mohu propojit nákupní objednávku s prodejní objednávkou, abych splnil/a poptávku?

Můžete vytvořit nákupní objednávku z prodejní objednávky. Další informace najdete ve [Vytvoření nákupní objednávky z prodejní objednávky](tasks/create-purchase-order-sales-order.md).

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a>Nemohu zrušit ani odstranit vratku nebo prodejní objednávku.

Můžete zrušit pouze prodejní objednávky a vratky, které jsou ve stavu *Vytvořeno*. Další informace naleznete v tématu [Zrušení vratky](../service-management/cancel-return-order.md).

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a>Při pokusu o zrušení prodejní objednávky se zobrazí chyba „Nelze odebrat rezervace, protože existuje práce, která závisí na rezervacích“.

Kód chyby: WAX4661

Pokud je práce přidružená k prodejní objednávce, nemůžete zrušit prodejní objednávku, dokud nebude práce zrušena a stornována. Tento požadavek platí, i když je práce přidružená k prodejní objednávce uzavřena.

Chcete-li opravit problém, postupujte následovně.

1. Zrušte práci a vložte zásoby zpět na požadované místo. Přejděte na příslušné vytížení prodejní objednávky a vyberte buď **Snížit vyskladněné množství** na řádku vytížení nebo **Stornovat práci** v podokně akcí.

    Práce má nyní stav *Zrušeno* a automaticky se vytvoří a zpracuje nová práce přesunu zásob, aby se zásoby vrátily zpět na místo, které bylo popsáno v době zrušení.

2. Odstraňte vytížení. Dodávka je také odstraněna.
3. Nyní byste měli být schopni přejít k prodejní objednávce a zrušit ji.

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a>Nemohu zrušit mezipodnikovou nákupní objednávku, která je propojena s prodejní objednávkou.

### <a name="issue-description"></a>Popis problému

Pokud se pokusíte zrušit mezipodnikovou nákupní objednávku, která je propojena s prodejní objednávkou, může se zobrazit následující chybová zpráva: „Množství nelze snížit, protože zbývající množství aktualizace mění znaménko.“

### <a name="issue-resolution"></a>Řešení problému

Tento problém byl opraven v Microsoft Dynamics 365 Supply Chain Management verze 10.0.13. V této a novějších verzích můžete nyní zrušit mezipodnikovou nákupní objednávku, která je propojena s prodejní objednávkou.

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>Mohu obnovit fakturovanou prodejní objednávku, která byla odstraněna?

### <a name="issue-description"></a>Popis problému

Fakturovaná prodejní objednávka byla omylem odstraněna a chcete ji obnovit nebo zobrazit její podrobnosti.

### <a name="issue-resolution"></a>Řešení problému

Pokud byla odstraněná prodejní objednávka již fakturována, přejděte na **Účet zákazníka \> Transakce \> Původní dokument \> Zobrazit podrobnosti**. Najděte fakturu, kterou hledáte, a jejím výběrem zobrazíte její podrobnosti. Mezi tyto podrobnosti patří odkaz na prodejní objednávku. Na této stránce byste také měli mít přístup k podrobnostem prodejní objednávky.

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a>Termín záhlaví prodejní objednávky nelze najít v datové entitě SalesOrderHeaderV2Entity.

Pole termínu neexistuje v entitě *SalesOrderHeaderV2Entity*.

## <a name="i-must-delete-orphaned-sales-order-records"></a>Musím odstranit osamocené záznamy prodejní objednávky.

Chcete-li vyčistit osamocené záznamy prodejní objednávky, spusťte periodickou úlohu *Odstranění prodejní objednávky* přechodem na jedno z následujících míst:

- Prodej a marketing \> Periodické úkoly \> Vyčistit \> Odstranit prodejní objednávky
- Retail a Commerce \> Retail a Commerce IT \> Vyčistit \> Odstranit prodejní objednávky

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>Existuje způsob, jak vypočítat provize z faktur, které již byly zaúčtovány?

Supply Chain Management aktuálně nepodporuje výpočet provizí za zaúčtované faktury.

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a>V mezipodnikovém procesu není položka sady podporována.

Položka sady není pro nákupní objednávku k dispozici, protože pokud prozkoumáte řádky prodejní objednávky pro položku sady, zjistíte, že množství je *0* (nula) a stav je *Zrušeno*. Toto chování je záměrné. Prodejní objednávka nakupuje pouze komponenty položky sady. Nezakupuje samotnou položku sady.

Pokud si musíte koupit sadu, zvažte, zda ji musíte označit jako položku sady, protože tato funkce je navržena pro scénáře rozpoznávání výnosů. Další informace o položkách sady naleznete v tématu [Sady](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]