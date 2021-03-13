---
title: Odesílání faktur do systému pracovních postupů a spárování řádků příjemek produktů
description: Toto téma vysvětluje proces odesílání importovaných faktur dodavatelů do systému workflow a párování zaúčtovaných řádků příjemek produktů s fakturami dodavatelů.
author: abruer
manager: AnnBe
ms.date: 09/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 03c9f6752a0bb9641f67d65580aca18276e43e9a
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115649"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines"></a>Odesílání faktur do systému pracovních postupů a spárování řádků příjemek produktů

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje proces odesílání importovaných faktur dodavatelů do systému workflow a párování zaúčtovaných řádků příjemek produktů s fakturami dodavatelů.

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a>Odesílání importovaných faktur dodavatelů do systému workflowu a párování zaúčtovaných řádků příjemky produktu s nevyřízenými řádky faktury dodavatele

V rámci bezobslužného procesu fakturace závazků můžete systém nechat automaticky odeslat importovanou fakturu do systému workflowu. Proces odesílání importovaných faktur do systému workflow můžete nakonfigurovat na kartě **Automatizace faktur dodavatele** stránky **Parametry závazků** (**Závazky \> Nastavení \> Parametry závazků**). Proces odeslání do pracovního postupu poběží na pozadí s frekvencí, kterou určíte (každou hodinu nebo každý den).

Když automaticky odesíláte faktury do systému workflow, musíte začít s importovanou fakturou. Aby fakturu bylo možné zpracovat od začátku až do konce bez ručního zásahu, musíte do konfigurace workflowu zahrnout automatizovanou úlohu zaúčtování. Do systému workflowu lze automaticky odesílat faktury, které souvisejí s nákupními objednávkami, a faktury, které obsahují kategorii zásobování bez nákupní objednávky a řádky, které nejsou na skladě. Faktury, které se zadávají ručně, je třeba ručně odeslat do systému workflow.

Hodnota **Odeslal** v pracovním postupu je ID uživatele, které bylo zadáno pro úlohu na pozadí **Odeslat faktury dodavatele do pracovního postupu** na stránce **Automatizace procesů**. Uživatel, který má toto ID uživatele, bude moct podle potřeby vyvolat fakturu ze systému workflow.

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a>Párování příjemek produktů s řádky faktur, které používají třícestné párování

V rámci bezdotykových procesů fakturace závazků může systém automaticky přiřazovat zaúčtované příjemky produktům k řádkům faktur. Pro tento úkol je třeba definovat zásadu třícestného párování. Tato funkce je k dispozici, pokud funkce **Automatizace faktur dodavatele** byla povolena na stránce **Správa funkcí**.

Proces poběží tak dlouho, dokud se spárované množství na příjemce produktu nebude rovnat množství na faktuře. U tohoto procesu můžete určit maximální počet pokusů, které má systém na spárování příjemky produktu s řádkem faktury, než se tento proces označí jako neúspěšný. Tento proces poběží na pozadí každou hodinu nebo každý den. Proces automatizovaného párování můžete spustit jako součást procesu odesílání faktur do systému workflowu. Můžete ho rovněž spustit jako samostatný proces. Nastavení procesu přiřazení příjemek produktů řádkám faktur se konfiguruje na kartě **Automatizace faktur dodavatele** stránky **Parametry závazků** (**Závazky \> Nastavení \> Parametry závazků**).

Řádky faktur, které mají zásadu třícestného párování, kde je spárované množství příjemky menší než množství faktury, budou zahrnuty do automatizovaného procesu párování s příjemkami produktů.

Chcete-li zobrazit stav **Poslední shoda** u faktur, které nejsou součástí procesu automatického odesílání do pracovního postupu, otevřete fakturu ze stránky **Faktury dodavatele**. Při zobrazení faktury se aktualizují informace pro ověření spárování. Stav **Poslední shody** lze automaticky aktualizovat pomocí úkolu na pozadí **Ověření shody faktur**. Můžete nakonfigurovat proces automatické aktualizace stavu **Poslední shoda** na kartě **Procesy na pozadí** na stránce **Procesní automatizace** (**Správa systému \> Nastavení \> Procesní automatizace**).

Řádek faktury bude vyloučen z automatizovaného zpracování, pokud bude splněna některá z následujících podmínek:

- Hodnota **Stav shody automatického potvrzení** řádku faktury je **Selhalo**.
- Faktura se používá.
- Faktura je v systému workflow.
