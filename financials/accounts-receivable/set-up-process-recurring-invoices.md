---
title: "Nastavení a zpracování opakovaných faktur"
description: "Tento článek vysvětluje, jak lze nastavit a zpracovat opakované faktury. Opakované faktury lze použít, pokud musíte pravidelně fakturovat odběrateli stejnou částku."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 463a81d615e6820b6ab45592cd21e28a76c6c04d
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-and-process-recurring-invoices"></a>Nastavení a zpracování opakovaných faktur

[!include[banner](../includes/banner.md)]


Tento článek vysvětluje, jak lze nastavit a zpracovat opakované faktury. Opakované faktury lze použít, pokud musíte pravidelně fakturovat odběrateli stejnou částku.

<a name="create-a-recurring-free-text-invoice-template"></a>Vytvoření šablony pro opakovanou volnou fakturu
---------------------------------------------

Pro fakturaci odběratelů za stejné služby v pravidelných intervalech je nutné definovat šablonu volné faktury, kterou lze opakovaně použít k vytvoření faktur. V šabloně jsou uvedeny následující informace:

-   Informace v záhlaví, jako jsou daňové skupiny, platební podmínky a způsob platby
-   Informace o řádku, například popis služby, účty výnosů, jednotková cena a fakturovaná částka
-   Náklady na dodání nebo zpracování
-   Rozúčtování společně s informacemi o finanční dimenzi, například nákladových střediscích nebo obchodních jednotkách

V důsledku vytváříte celou fakturu a ukládáte ji jako šablonu. Šablony můžete nastavit pomocí stránky **Opakované faktury**.

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a>Přiřazení šablony volné faktury odběrateli a zadání podrobností o opakování
Po vytvoření šablony je nutné přiřadit šablonu zákazníkům, kterým má být vystavena. Dále zadejte, kdy a jak často se má fakturovat. Šablony můžete přiřadit na kartě **Faktury** na stránce **Odběratelé**. Přidejte šablonu do seznamu a aktualizujte následující informace:

-   Počáteční datum a případně koncové datum pro opakování účtování
-   Frekvence opakování fakturace (například každý den nebo jednou za měsíc)
-   Maximální částka účtování (pokud jsou tyto informace požadovány)

Zákazník může mít více šablon, které mají různé intervaly.

## <a name="generate-the-recurring-invoices"></a>Generování opakovaných faktur
Na stránce **Opakované faktury** je úkol, který zpracovává šablony opakovaných faktur. Určete datum faktury a šablonu, ze které se mají faktury generovat. Faktury budou generovány a každé skupině zpracovaných faktur se přiřadí jedno ID opakování.
Zaúčtování opakovaných volných faktur
---------------------------------

Po vygenerování opakovaných faktur se ID opakování faktury objeví v zaúčtování úloh stránce **Opakované faktury**. Všechny faktury se stejným ID opakování si můžete prohlédnout kliknutím na odkaz. Během kontroly faktur podle ID opakování lze jednotlivé faktury odstranit. Nastavení opakování se u šablony odběratele obnoví, aby se mohla znovu generovat později. Zaúčtovat můžete jednu, více nebo všechny faktury pro ID opakování. Jsou-li workflowy povolené, je nutné před zaúčtováním faktury kliknout na tlačítko **Odeslat**.
Tisk opakovaných volných faktur
----------------------------------

Po zaúčtování opakované faktury můžete faktury vytisknout ze stránky se seznamem volných faktur. Lze vytisknout vybrané faktury nebo vybrat rozsah faktur k tisku.




