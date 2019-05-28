---
title: Povolení procesu mezd pro čas a docházku
description: Tento postup popisuje, jak povolit mzdový proces pro čas a docházku.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0174f438396d814d153befe4a59a79b6eebb2288
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560176"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a>Povolení procesu mezd pro čas a docházku

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak povolit mzdový proces pro čas a docházku. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="create-a-pay-type-with-a-related-pay-rate"></a>Vytvoření typu mzdy podle související mzdové sazby
1. Čas a docházka > Nastavení > Platba > Typy mezd
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Typ mzdy.
4. Zadejte nějakou hodnotu do pole Popis.
5. Klikněte na položku Uložit.
6. Klepněte na tlačítko Sazby.
    * Sazby typů mezd se nastavují pro příslušné časové intervaly a jednotlivé sazby lze vytvořit zaměstnance. Není vždy nutné, abyste sazby vytvářeli pro typy mezd podle času a docházky. Tato informace může již existovat v systému mezd, který slouží ke generování mezd.  
7. Klikněte na položku Nová.
8. Označte v seznamu vybraný řádek.
9. Do pole Sazba zadejte číslo.
10. Klikněte na položku Uložit.

## <a name="create-a-pay-agreement"></a>Vytvoření mzdové smlouvy
1. Zavřete stránku.
2. Zavřete stránku.
3. Přejděte na Platební smlouvy.
    * Čas a docházka > Nastavení > Platební smlouvy  
4. Klikněte na položku Nová.
5. Zadejte hodnotu do pole Platební smlouva.
6. Zadejte nějakou hodnotu do pole Popis.
7. Klikněte na položku Uložit.
8. Klikněte na Řádky smlouvy.
9. Klikněte na položku Nová.
10. Označte v seznamu vybraný řádek.
11. V poli Typ profilu zadejte nebo vyberte hodnotu.
12. V poli Typ mzdy zadejte nebo vyberte hodnotu.

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a>Nastavení platební dohody pro čas a registraci pracovníka
1. Zavřete stránku.
2. Zavřete stránku.
3. Přejděte na Pracovníci registrace času.
    * Čas a docházka > Nastavení > Pracovníci registrace času  
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Klikněte na kartu Zaměstnání.
6. Rozbalte položku Časová registrace.
7. Klikněte na položku Upravit.
8. V poli Platební smlouva zadejte nebo vyberte hodnotu.

