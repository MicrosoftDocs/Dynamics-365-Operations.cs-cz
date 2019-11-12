---
title: Fakturování projektu
description: V tomto článku najdete přehled fakturace projektu pro časové a materiálové projekty a projekty s pevnou cenou. Zahrnuje informace o návrzích faktur (předběžné faktury), řízení faktur, fakturování na účet, fakturaci dodavatele a dobropisech.
author: ShylaThompson
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjInvoiceCashFlow, ProjInvoiceControl, ProjInvoiceListPage, ProjInvoiceProposalDetail, ProjInvoiceProposalListPage
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23111
ms.assetid: 1812d6f2-8b34-4258-8f5f-dcf12281547f
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a68ed1cf21039ec1077bae428dea242f19514b51
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658613"
---
# <a name="project-invoicing"></a>Fakturování projektu

[!include [banner](../includes/banner.md)]

V tomto článku najdete přehled fakturace projektu pro časové a materiálové projekty a projekty s pevnou cenou. Zahrnuje informace o návrzích faktur (předběžné faktury), řízení faktur, fakturování na účet, fakturaci dodavatele a dobropisech.

Typ projektu stanoví, který fakturační postup by měl být použit. Fakturovat lze pouze dva typy externích projektů – časový a materiálový projekt nebo projekt s pevnou cenou. Časové a materiálové projekty a projekty s pevnou cenou jsou vždy připojeny k projektové smlouvě.

-   **Projekty s pevnou cenou** – Částka fakturovaná odběrateli je založena na plánech účtování faktur. Fakturace se provádí prostřednictvím nastavení na účet, někdy označovaného také jako plán účtování. Projekty s pevnou cenou mohou být fakturovány za projekt nebo za projektovou smlouvu.
-   **Časové a materiálové projekty** – Částka fakturovaná odběrateli je založena na řádcích transakcí zadaných do projektů. Transakce mohou být fakturovány za projekt nebo za projektovou smlouvu.

Existují tři možnosti připojení časových a materiálových projektů a projektů s pevnou cenou k fakturačním projektům:

-   **Akontační fakturace** – Časové a materiálové projekty a projekty s pevnou cenou lze fakturovat na účet. Jsou vyžadovány dva typy akontačního nastavení, jeden pro každý typ projektu.
-   **Fakturace v periodické části** – Prostřednictvím periodické funkce lze transakce fakturovat mezi projekty. Periodické funkce poskytují přehled transakcí, které musí být fakturovány.
-   **Použitím dobropisů ve fakturách** – Dobropis lze vytvořit jak pro časové a materiálové projekty, tak pro projekty s pevnou cenou.

## <a name="invoice-proposals"></a>Návrhy faktur
Před vytvořením faktury odběratele pro projekt můžete vytvořit předběžnou fakturu nebo návrh faktury. Do návrhu faktury můžete vybrat projektové transakce, které mají být zahrnuty do faktury projektu. Poté můžete zobrazit podrobnosti faktury před zaúčtováním faktury projektu a jejím odesláním odběrateli nebo jinému zdroji financování.

### <a name="creating-invoice-proposals"></a>Vytváření návrhů faktur

Návrhy faktur můžete vytvořit ručním výběrem ze seznamu transakcí pro zadaný projekt. Můžete také nastavit pravidla účtování, která určují, kdy chcete automaticky vytvořit návrh faktury. Například můžete vytvořit pravidlo účtování k vytvoření návrhu faktury při dokončení 25, 50, 75 nebo 100 procent práce na projektu. 

Návrhy faktury mohou být vytvořeny pro následující transakce:

-   Hodiny, výdaje a další transakce projektu
-   Částky, které jsou zadrženy odběrateli na předchozích fakturách projektů
-   Dobropisy
-   Částky, které jsou vám zaplaceny odběratelem před zahájením projektu

> [!NOTE]
> Funkce **Povolit řazení podle zdroje během funkce vytvoření návrhu faktury projektu** umožňuje účetním projektu řadit transakce projektu, které jsou k dispozici pro účtování zdroje při vytváření nového návrhu faktury projektu. Mřížka zobrazující dostupné projektové transakce bude mít samostatné pole pro ID prostředku a prostředek, což uživateli umožňuje filtrovat a řadit podle názvu prostředku. Tato funkce je ve výchozím nastavení zakázána a lze ji povolit v části **Pracovní prostory > Správa funkcí**. Chcete-li pomoci s povolením této funkce, obraťte se na správce systému.

V návrhu faktury lze vytvořit transakce poplatků. Můžete také změnit prodejní cenu za hodinu, výdaj, položku a transakce poplatků. Při zaúčtování návrhu faktury jsou přidány aktualizované ceny a transakce do sestav projektů a historie transakcí. 

Pokud chcete vytvořit více faktur odběratelů pro určitý projekt, je nutné vytvořit návrh faktury pro každou fakturu. Můžete například vytvořit faktury podle typu transakce. Pokud chcete zadat hodiny na jedné faktuře odběratele a položky na jiné, je nutné vytvořit samostatný návrh faktury pro hodinové transakce a samostatný návrh faktury pro transakce poplatků. 

Pokud projekt má více než jeden zdroj financování, můžete vytvořit samostatný návrh faktury pro každý zdroj financování. Na stránce **Přidělení pravidel financování** lze definovat procento částky transakce, které má být přiděleno jednotlivým zdrojům financování, a zdroj, kterému chcete zaúčtovat rozdíly zaokrouhlení.

### <a name="creating-customer-invoices-from-invoice-proposals"></a>Vytváření faktur odběratele z návrhů faktury

Po vytvoření a zaúčtování návrhu faktury bude automaticky vytvořena faktura odběratele pro transakce, které jsou zahrnuty do návrhu faktury. 

Před zaúčtováním návrhu faktury lze přidat nebo odstranit transakce. Například můžete odebrat výdajové transakce, které byly zaúčtovány v projektu, ale nejsou fakturovatelné odběrateli. 

Pokud vaše organizace vyžaduje, aby byly návrhy faktury před zaúčtováním zkontrolovány, může být před zaúčtováním návrhu faktury vyžadováno schválení pomocí workflowu "Zkontrolovat návrhy faktury projektu".

## <a name="on-account-invoicing"></a>Faktura akontace
Částka, kterou zadáte do faktury na účet pro projekt, je založena na časovém období, procentuální hodnotě dokončení a dalších podmínkách fakturace, které jsou zadány v související projektové smlouvě. Částka není založena na hodinách, položkách, výdajích ani poplatcích, které jsou zaúčtovány do projektu. 

Je nutné nejprve vytvořit transakci na účet pro časový a materiálový projekt nebo projekt s pevnou cenou, abyste mohli přidat transakci na účet pro fakturu projektu. V transakci na účet zadejte částku faktury odběratele. Chcete-li vytvořit fakturu projektu pro částku, vytvořte předběžnou fakturu (návrh faktury). V návrhu faktury vyberte transakci na účet. Můžete zkontrolovat informace na účet v návrhu faktury, než pro ni vytvoříte fakturu projektu.

### <a name="fixed-price-projects"></a>Projekty s pevnou cenou

Pro projekty s pevnou cenou jsou transakce na účet založeny na dohodnutém milníku, jednotce dodání nebo průběžném účtování, které jsou zadány ve smlouvě projektu. Pro každou platbu bude vytvořen jeden řádek, který musí být přijat od odběratele projektu. Nejsou vyžadovány srážky.

### <a name="time-and-material-projects"></a>Časové a materiálové projekty

U časových a materiálových projektů je možné účtovat odběratele nebo jiný zdroj financování pro částku zálohy pomocí návrhu faktury na účet. Zadejte transakce na účet jako jeden řádek. Volitelně můžete zadat další řádky jako odpočty pro vyrovnání všech záloh, které již zákazník provedl. K vytvoření řádků odpočtu před částku uveďte záporné znaménko.

## <a name="invoice-control"></a>Řízení faktury
Řízení faktury slouží ke sledování fakturovaných a nefakturovaných transakcí a k analýze těchto transakcí vzhledem k nabídkám pro kompletní zobrazení projektů od fáze nabídky až po dokončení. Lze zobrazit, které transakce byly vyúčtovány u určitého projektu a které řádky byly fakturovány. Můžete rovněž zobrazit jednotlivé transakce, abyste je mohli upravit po zaúčtování.

## <a name="invoicing-fixed-price-projects"></a>Fakturace projektů s pevnou cenou
Chcete-li fakturovat projekt s pevnou cenou, můžete definovat plán účtování a dokončit fakturační postup.

### <a name="billing-schedule"></a>Plán účtování

Můžete fakturovat projekty s pevnou cenou dle plánu účtování. Plán účtování je definován v souvislosti s jedním nebo více milníky pro projekt. Pro každý milník můžete definovat určité datum, prodejní měnu, prodejní cenu a aktivitu. 

Můžete vytvářet například následující plán účtování:

-   20 procent při podpisu projektové smlouvy
-   30 procent první dodávce
-   15 procent druhé dodávce
-   35 procent poslední dodávce

### <a name="invoicing-procedure"></a>Fakturační postup

Když jsou milníkové platby připraveny k fakturaci, použijte postup fakturace částek na účet.

## <a name="vendor-invoicing"></a>Fakturace dodavatele
Při objednání zboží od dodavatele a přiřazená zboží k projektu určuje vlastnost položky, kterou vyberete pro řádek nákupní objednávky, zda bude nakoupená položka fakturována odběrateli. Pokud jste nastavili výchozí vlastnosti řádku, jsou zobrazeny pro položku na řádku nákupní objednávky (Podrobnosti řádku &gt; Projekt &gt; Vlastnost řádku). Existují dva způsoby, jak změnit vlastnost řádku:

-   Fakturovat odběrateli projektu za zboží: Nastavte vlastnost řádku pro položku na fakturovatelnou hodnotu na nákupní objednávce a následně fakturujte odběrateli pomocí správného způsobu fakturace projektu.
-   Nefakturovat odběrateli projektu za zboží: Nevybírejte vlastnost řádku **Fakturovatelné** na řádku nákupní objednávky pro položku. Poté lze nákupní objednávku vyfakturovat a není třeba provádět další akce.

## <a name="credit-notes"></a>Dobropisy
Je-li na faktuře odběratele uvedena záporná částka, považuje se takový doklad za dobropis. Při tisku dokumentu nese název "Dobropis". 

Když vytváříte dobropis na částku, která byla v minulosti fakturována, musíte nejprve vybrat fakturovanou částku, kterou chcete dobropisovat. Potom vytvořte dobropis úplně stejným způsobem, jaký používáte k vytvoření běžné faktury odběratele. Jinými slovy musíte vybrat transakce, které byly dříve zaúčtovány pro fakturu odběratele a pak vytvořit a zaúčtovat návrh dobropisu. 

Stejný dokument může obsahovat transakce, které jsou vybrané k dobropisování, transakce dobropisu i transakce, které byly zaúčtovány. Dokument je klasifikován jako faktura nebo dobropis, v závislosti na znaménku celkové částky. 

Chcete-li dopropisovat fakturovanou částku, musíte nejprve vybrat fakturovanou částku, kterou chcete dobropisovat, a poté vytvořit dobropis. Vytvořte dobropis úplně stejným způsobem, jaký používáte k vytvoření běžné faktury odběratele. 

Můžete vytvořit fakturu se zápornou částkou, což bude faktura klasifikovaná jako dobropis. Chcete-li vytvořit a vytisknout dobropis, musíte vybrat transakce, které byly dříve zaúčtovány pro fakturu odběratele, a pak upravit transakce. Pokud není primární adresa právnické osoby v Německu, je název faktury "Opravná faktura".



