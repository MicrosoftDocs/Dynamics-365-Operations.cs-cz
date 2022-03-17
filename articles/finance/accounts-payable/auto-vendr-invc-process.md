---
title: Přehled procesů automatizované fakturace dodavatelů
description: Toto téma popisuje možnosti automatizace zpracování faktur dodavatelů a výhody používání automatizovaného procesu.
author: abruer
ms.date: 02/12/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-08-30
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f21b76bb0d30370e4ea4fdd718999d537e9ce925
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358418"
---
# <a name="automated-vendor-invoicing-processes-overview"></a>Přehled procesů automatizované fakturace dodavatelů

[!include [banner](../includes/banner.md)]

Toto téma popisuje možnosti automatizace zpracování faktur dodavatelů a výhody používání automatizovaného procesu. Tato schopnost se skládá z funkcí, které se zapínají ve Správě funkcí. Tyto funkce se vztahují pouze na faktury dodavatelů, nikoli na faktury zpracovávané prostřednictvím stránky **Deník faktur** nebo **Deník registru faktur**.

Organizace často svěřují zpracování papírových faktur třetím stranám, které používají některého poskytovatele služeb optického rozpoznávání znaků (OCR). Poskytovatel služeb vrací strojově čitelná metadata faktur. Funkce automatizace závazků umožňují tyto artefakty ze závazků používat, což vám pomůže při automatizaci.

Některé procesy fakturace závazků dodavatelů můžete automatizovat. Mezi tyto procesy patří odesílání importovaných faktur dodavatelů do systému workflowu a párování zaúčtovaných řádků příjemky produktu s nevyřízenými řádky faktury dodavatele. Automatizovaný proces zobrazuje informace o tom, jak faktura dodavatele postupuje každým z těchto procesů. Tato funkce dokáže účetním a manažerům oddělení závazků pomoci s efektivnějším zpracováním faktur dodavatelů. Pomáhá rovněž omezit chyby a neefektivity, ke kterým může dojít při ručním zadávání a zpracování informací.

Procesy automatizace umožňují:

- Automatické použití záloh na faktury dodavatele
- Automaticky odesílat importované faktury do systému workflowu.
- Párovat příjemky produktu s nevyřízeními řádky faktury dodavatele.
- Simulovat zaúčtování před zaúčtováním faktury dodavatele.
- Rychle a efektivně zobrazit historii workflowu a automatizace.
- Zobrazit a analyzovat výsledky automatizovaného zpracování faktur dodavatelů.
- Obnovit automatizované zpracování více faktur.

## <a name="submit-imported-vendor-invoices-to-the-workflow-system"></a>Odesílání importovaných faktur dodavatele do systému pracovního postupu

V rámci bezobslužného procesu fakturace závazků může být importovaná faktura automaticky odeslána do systému pracovního postupu. Tento proces poběží na pozadí s frekvencí, kterou určíte (každou hodinu nebo každý den). Funkce automatického odesílání importovaných faktur do systému workflowu vyžaduje, aby tento proces začínal importovanou fakturou. Aby fakturu bylo možné zpracovat od začátku až do konce bez ručního zásahu, musí být do konfigurace workflowu zahrnuta automatizovaná úloha zaúčtování.


Do systému workflowu lze automaticky odesílat faktury, které souvisejí s nákupními objednávkami, a faktury, které obsahují kategorii zásobování bez nákupní objednávky a řádky, které nejsou na skladě. Faktury, které se zadávají ručně, a faktury, které se vytvářejí prostřednictvím pracovního prostoru **Fakturace dodavatelské spolupráce**, musí být do systému workflowu odeslány ručně. Zpracování žádosti o platbu předem musí být u importovaných faktur provedeno ručně. Zálohy můžete použít ručně před nebo po zaúčtování importované faktury. Na nezaúčtované standardní faktury můžete ručně použít zálohy pomocí stránky **Faktury dodavatele**. Po zaúčtování bude vypořádaná záloha k dispozici k ručnímu uplatnění na další faktury od tohoto dodavatele na stránce **Dodavatelé** (**Pohledávky \> Společné \> Dodavatelé \> Všichni dodavatelé \> Karta Faktura \> Použít**).

Funkce automatizace poskytuje flexibilní rámec, který umožňuje definovat firemně specifická pravidla pro odesílání importovaných faktur dodavatelů do systému workflowu a párování zaúčtovaných řádků příjemky produktu s nevyřízenými řádky faktury dodavatele.

## <a name="match-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Párování příjemek produktů s řádky faktur, které používají třícestné párování

Zaúčtované příjemky produktů mohou být automaticky spárovány s řádky faktur, pro které je definováno třícestné párování. Proces poběží tak dlouho, dokud se spárované množství na příjemce produktu nebude rovnat množství na faktuře. U tohoto procesu můžete určit maximální počet pokusů, které má systém na spárování příjemky produktu s řádkem faktury, než se tento proces označí jako neúspěšný. Tento proces poběží na pozadí každou hodinu nebo každý den. Proces automatizovaného párování můžete spustit jako součást procesu odesílání faktur do systému workflowu. Můžete ho rovněž spustit jako samostatný proces.

## <a name="pre-validate-vendor-invoice-posting"></a>Předběžné zaúčtování faktur dodavatele

Simulace zaúčtování dokončuje postup ověření, který se provádí během procesu zaúčtování faktur dodavatelů, nejsou ale aktualizovány žádné účty. Tento proces spustíte tak, že na stránce **Nevyřízené faktury dodavatelů** vyberete jednu fakturu nebo několik faktur.

## <a name="enhanced-experience-for-viewing-workflow-and-automation-historical-information-for-vendor-invoices"></a>Vylepšené prostředí pro prohlížení historických informací pracovního postupu a automatizace faktur dodavatelů

K dispozici je přehledné zobrazení historie workflowu faktur dodavatelů. K historii workflowu faktury dodavatele se lze dostat přímo z faktury dodavatele. K nalezení těchto informací je tedy zapotřebí méně kliknutí. Pokud vaše organizace povolila možnost automaticky odesílat importované faktury dodavatelů do workflowu, je pro importované faktury poskytnuta historie automatizace. Historie automatizace vám pomůže identifikovat aktuální krok procesu i kroky, které již byly dokončeny. Pokud je krok neúspěšný, získáte podrobné informace, které vám pomohou pochopit důvod selhání.

## <a name="analytics-and-metrics"></a>Analýza a metriky

Pracovní prostor **Zadání faktury dodavatele** vám umožňuje se plně soustředit na faktury dodavatelů, které neprošly automatizovaným procesem. Na dlaždicích tohoto pracovního prostoru jsou uvedeny informace o fakturách dodavatelů, které nebyly úspěšně odeslány do systému workflowu, importovány nebo spárovány s příjemkami produktů. K dispozici jsou rovněž metriky Microsoft Power BI, které manažerům oddělení závazků poskytují přehled o efektivitě automatizace faktur dodavatelů.


## <a name="resume-automation-processing-for-multiple-invoices"></a>Obnovení automatizovaného zpracování více faktur

Pokud importovaná faktura není úspěšně odeslána do pracovního postupu prostřednictvím automatizovaného procesu, systém ji odebere z dalšího automatizovaného zpracování. Úředník pro závazky může zkontrolovat a upravit fakturu, než ji automatický proces znovu odešle do workflowu. Pokud lze důvod selhání vyřešit stejnou opravou pro více faktur, můžete restartovat automatizovaný proces na stránce **Obnovit automatické zpracování faktur**. 

## <a name="tracking-the-invoice-received-date-value"></a>Sledování hodnoty data přijetí faktury

Hodnota **Datum přijetí faktury** označuje datum, kdy společnost obdržela fakturu od dodavatele. Poskytuje výchozí bod pro sledování průběhu faktury prostřednictvím automatizačních procesů. Tuto hodnotu lze zahrnout do importovaných dat pro fakturu dodavatele. U faktur, které byly vytvořeny ručně, můžete určit datum. Pokud není zadána žádná hodnota, použije se ve výchozím nastavení aktuální datum.


## <a name="tracking-the-imported-invoice-amount-and-imported-sales-tax-amount-values"></a>Sledování hodnot importované částky faktury a importované částky DPH

Hodnota **Importovaná částka faktury** a **Importovaná částka DPH** pro faktury dodavatele lze zadat v souboru importu faktur dodavatele. Tyto hodnoty obvykle pocházejí z faktury, která byla naskenována externím poskytovatelem a zahrnuta do souboru pro import. Protože je faktura zpracovávána v položce Účty splatné, budou hodnoty vypočítány na základě údajů z faktury. Fakturu lze zaúčtovat, pouze pokud se importované hodnoty shodují s vypočítanými hodnotami. Odpovídající hodnoty zajišťují, že faktura přesně odráží částku splatnou dodavateli. Pokud vaše organizace umožňuje automatické odesílání importovaných faktur do systému pracovních postupů, můžete volitelně požadovat, aby se importované součty shodovaly s vypočítanými součty, než bude možné odeslat fakturu do systému pracovních postupů.

## <a name="vendor-invoice-automation---resume-automation-processing-for-multiple-invoices"></a>Automatizace faktur dodavatele – pokračujte v automatizovaném zpracování více faktur
Pokud importovaná faktura není úspěšně odeslána do pracovního postupu prostřednictvím automatizovaného procesu, bude odebrána z dalšího automatizovaného zpracování. Úředník pro závazky může zkontrolovat a upravit fakturu, než ji automatický proces znovu odešle do workflowu. Pokud lze důvod selhání vyřešit stejnou opravou pro více faktur, můžete restartovat automatizovaný proces na stránce **Obnovit automatické zpracování faktur**. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
