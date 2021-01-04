---
title: Odstraňování problémů s rozpočtováním pozice
description: Tento článek obsahuje odpovědí na otázky, které můžete mít při konfiguraci rozpočtování pozice. Řeší časté otázky týkající se vytváření prvků rozpočtových nákladů, skupin kompenzací a kompenzačních mřížek.
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: afddc9815ee3864236f93c8400bcf116d5b6cc89
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441246"
---
# <a name="position-budgeting-troubleshooting"></a>Odstraňování problémů s rozpočtováním pozice

[!include [banner](../includes/banner.md)]

Tento článek obsahuje odpovědí na otázky, které můžete mít při konfiguraci rozpočtování pozice. Řeší časté otázky týkající se vytváření prvků rozpočtových nákladů, skupin kompenzací a kompenzačních mřížek. 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a>Proč nelze najít stránku s pozicí prognózy v modulu Lidské zdroje?
---------------------------------------------------------------

Pozice prognózy byly přesunuty do modulu Rozpočtování.

## <a name="why-cant-i-delete-a-budget-cost-element"></a>Proč nelze odstranit prvek rozpočtových nákladů?
Nelze odstranit prvek rozpočtových nákladů, který je přiřazen k jedné pozici prognózy. Před odstraněním prvku rozpočtových nákladů jej odeberte ze všech pozic prognózy. **Tip:** Pokud chcete vyhledat všechny pozice, ke kterým je přiřazen prvek rozpočtových nákladů, vyberte nákladový prvek na stránce **Prvky rozpočtových nákladů** a klepněte na tlačítko **Aktualizovat pozice**. Pozice, které používají nákladový prvek, jsou uvedeny v horní mřížce.

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a>Jak je možné odebrat nákladový prvek z několika pozic prognózy bez jejich jednotlivého otevření?
Prvek nákladů nelze odstranit. Pokud ale změníte počáteční a koncové datum tak, aby spadalo mimo data cyklu plánování rozpočtu, nebude již přiřazen pozicím prognóz v daném cyklu plánování rozpočtu. Chcete-li provést tuto změnu, otevřete prvek rozpočtových nákladů a poté na pevné záložce **Výpočet nákladů** klepněte na tlačítko **Změnit data** a změňte datum začátku platnosti nebo datum vypršení platnosti. Klepnutím na **OK** automaticky aktualizujete všechny pozice prognózy, ke kterým je přiřazen nákladový prvek. **Tip:** Pokud použijete tuto metodu, pamatujte, že dojde k odebrání prvku rozpočtových nákladů ze **VŠECH** pozic prognózy, ve kterých počáteční a koncové datum již není v příslušném rozsahu. Pokud to nemáte v úmyslu, bude třeba otevřít jednotlivé pozice prognózy, ze kterých chcete odebrat prvek rozpočtových nákladů, a provést změny ručně.

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a>Proč nelze zadat roční částku na pevné kartě výpočtu nákladů prvku rozpočtových nákladů?
Nelze zadat roční částku, pokud existují prvky rozpočtových nákladů na pevné kartě **Základ výpočtu**, protože systém vyžaduje pro výpočet hodnoty procento. Odeberte všechny prvky rozpočtových nákladů z pevné karty **Základ výpočtu**, chcete-li tuto hodnotu měnit.

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a>Proč nelze změnit typ rozpočtových nákladů z hodnoty „příjmový“ na jiný typ rozpočtových nákladů?
Některé prvky rozpočtových nákladů používají nákladový prvek typu „příjmový“ jako základ pro výpočty. Chcete-li změnit pole **Typ rozpočtových nákladů**, odeberte prvek nákladový příjmů z pevné záložky **Základ výpočtu** u všech prvků rozpočtových nákladů.

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a>Proč nelze změnit datum řádků prvku rozpočtových nákladů pro prvek rozpočtových nákladů?
Datum na řádku prvku rozpočtových nákladů při použití prvku rozpočtových nákladů v pozici prognózy nelze změnit. Důvodem je, že je třeba zajistit, aby pozice prognóz byly vždy v souladu s pokyny prvku rozpočtových nákladů. Pokud chcete změnit datum, na pevné záložce **Výpočet nákladů** klepněte na tlačítko **Změnit data** a zadejte nové datum. Klepnutím na **OK** aktualizujete pozice, ke kterým je přiřazen nákladový prvek.

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a>Proč nelze změnit náklady pro prvek rozpočtových nákladů na stránce skupiny kompenzace?
Prvky rozpočtových nákladů můžete vytvářet a měnit pouze na stránce **Prvky rozpočtových nákladů**.

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a>Proč se zobrazila chybová zpráva při změně data pro nákladový prvek v pozici prognózy?
Data na řádku nákladového prvku pozice prognózy musí spadat do následujících rozsahů:

-   Data aktivace a vyřazení pozice.
-   Data aktivace a vypršení platnosti prvku rozpočtových nákladů.
-   Datum zahájení a ukončení rozpočtového cyklu, který j přidruženy k procesu plánování rozpočtu pozice prognózy.




