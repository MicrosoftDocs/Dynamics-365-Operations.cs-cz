---
title: Přehled procesů automatizované fakturace dodavatelů
description: Toto téma popisuje možnosti automatizace zpracování faktur dodavatelů a výhody používání automatizovaného procesu.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ec3598ebd158cc23ac7c02d7e33557141d5901bc
ms.sourcegitcommit: 9e7ceb5604472f3088f611aa0360bd6a716db32b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022489"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Přehled procesů automatizované fakturace dodavatelů

[!include [banner](../includes/banner.md)]

Toto téma popisuje možnosti automatizace zpracování faktur dodavatelů a výhody používání automatizovaného procesu. Tato schopnost se skládá z funkcí, které se zapínají ve Správě funkcí. Tyto funkce se vztahují pouze na faktury dodavatelů, nikoli na faktury zpracovávané prostřednictvím stránky **Deník faktur** nebo **Deník registru faktur**.

Organizace často svěřují zpracování papírových faktur třetím stranám, které používají některého poskytovatele služeb optického rozpoznávání znaků (OCR). Poskytovatel služeb vrací strojově čitelná metadata faktur. Funkce automatizace závazků umožňují tyto artefakty ze závazků používat, což vám pomůže při automatizaci.

Některé procesy fakturace závazků dodavatelů můžete automatizovat. Mezi tyto procesy patří odesílání importovaných faktur dodavatelů do systému workflowu a párování zaúčtovaných řádků příjemky produktu s nevyřízenými řádky faktury dodavatele. Automatizovaný proces zobrazuje informace o tom, jak faktura dodavatele postupuje každým z těchto procesů. Tato funkce dokáže účetním a manažerům oddělení závazků pomoci s efektivnějším zpracováním faktur dodavatelů. Pomáhá rovněž omezit chyby a neefektivity, ke kterým může dojít při ručním zadávání a zpracování informací.

Procesy automatizace umožňují:

- Automaticky odesílat importované faktury do systému workflowu
- Párovat příjemky produktu s nevyřízeními řádky faktury dodavatele
- Simulovat zaúčtování před zaúčtováním faktury dodavatele
- Rychle a efektivně zobrazit historii workflowu
- Zobrazit a analyzovat výsledky automatizovaného zpracování faktur dodavatelů

## <a name="vendor-invoice-automation--submit-imported-vendor-invoices-to-the-workflow-system"></a>Automatizace faktur dodavatelů – odeslání importovaných faktur dodavatele do systému workflowu

V rámci bezobslužného procesu fakturace závazků můžete systém nechat automaticky odeslat importovanou fakturu do systému workflowu. Tento proces poběží na pozadí s frekvencí, kterou určíte (každou hodinu nebo každý den). Funkce automatického odesílání importovaných faktur do systému workflowu vyžaduje, aby tento proces začínal importovanou fakturou. Aby fakturu bylo možné zpracovat od začátku až do konce bez ručního zásahu, musí být do konfigurace workflowu zahrnuta automatizovaná úloha zaúčtování.

Do systému workflowu lze automaticky odesílat faktury, které souvisejí s nákupními objednávkami, a faktury, které obsahují kategorii zásobování bez nákupní objednávky a řádky, které nejsou na skladě. Faktury, které se zadávají ručně, a faktury, které se vytvářejí prostřednictvím pracovního prostoru **Fakturace dodavatelské spolupráce** , musí být do systému workflowu odeslány ručně.

Funkce automatizace poskytuje flexibilní rámec, který umožňuje definovat firemně specifická pravidla pro odesílání importovaných faktur dodavatelů do systému workflowu a párování zaúčtovaných řádků příjemky produktu s nevyřízenými řádky faktury dodavatele.

## <a name="vendor-invoice-automation--match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Automatizace faktur dodavatelů – párování příjemek produktů s řádky faktur, které používají třícestné párování

Tento systém dokáže automaticky párovat zaúčtované příjemky produktů s řádky faktur, pro které je definováno třícestné párování. Proces poběží tak dlouho, dokud se spárované množství na příjemce produktu nebude rovnat množství na faktuře. U tohoto procesu můžete určit maximální počet pokusů, které má systém na spárování příjemky produktu s řádkem faktury, než se tento proces označí jako neúspěšný. Tento proces poběží na pozadí každou hodinu nebo každý den. Proces automatizovaného párování můžete spustit jako součást procesu odesílání faktur do systému workflowu. Můžete ho rovněž spustit jako samostatný proces.

## <a name="vendor-invoice-automation--pre-validate-vendor-invoice-posting"></a>Automatizace faktur dodavatelů – předběžné ověření zaúčtování faktur dodavatelů

Simulace zaúčtování dokončuje postup ověření, který se provádí během procesu zaúčtování faktur dodavatelů, nejsou ale aktualizovány žádné účty. Tento proces spustíte tak, že na stránce **Nevyřízené faktury dodavatelů** vyberete jednu fakturu nebo několik faktur.

## <a name="vendor-invoice-automation--enhanced-experience-for-viewing-workflow-historical-information-for-vendor-invoices"></a>Automatizace faktur dodavatelů – vylepšené prostředí pro prohlížení historických informací workflowu o fakturách dodavatelů

K dispozici je přehledné zobrazení historie workflowu faktur dodavatelů. K historii workflowu faktury dodavatele se lze dostat přímo z faktury dodavatele. K nalezení těchto informací je tedy zapotřebí méně kliknutí.

## <a name="vendor-invoice-automation--analytics-and-metrics"></a>Automatizace faktur dodavatelů – analýza a metriky

Pracovní prostor **Zadání faktury dodavatele** vám umožňuje se plně soustředit na faktury dodavatelů, které neprošly automatizovaným procesem. Na dlaždicích tohoto pracovního prostoru jsou uvedeny informace o fakturách dodavatelů, které nebyly úspěšně odeslány do systému workflowu, importovány nebo spárovány s příjemkami produktů. K dispozici jsou rovněž metriky Microsoft Power BI, které manažerům oddělení závazků poskytují přehled o efektivitě automatizace faktur dodavatelů.
