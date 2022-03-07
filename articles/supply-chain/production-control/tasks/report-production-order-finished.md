---
title: Ohlášení výrobní zakázky jako dokončené
description: Tato procedura popisuje způsob nahlásit výrobní zakázky jako dokončenou.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdParmReportFinished, ProdJournalTransProd, ProdSetupReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa27691942b27886e85c52b7b3a736a62db7b7bd
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7580593"
---
# <a name="report-a-production-order-as-finished"></a>Ohlášení výrobní zakázky jako dokončené

[!include [banner](../../includes/banner.md)]

Tato procedura popisuje způsob nahlásit výrobní zakázky jako dokončenou. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF. Jedná se o šestou proceduru ze sedmi, která vysvětluje životního cyklus výrobní zakázky.


## <a name="report-a-production-order-as-finished"></a>Ohlášení výrobní zakázky jako dokončené
1. Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.
    * Vyberte výrobní zakázku, která má stav Zahájeno.  
2. V podokně akcí klikněte na položku Výrobní zakázka.
3. Klikněte na položku Oznámit jako dokončené.
    * Na této stránce můžete potvrdit množství dokončeného produktu, které má být ohlášeno jako dokončené.  
4. Klikněte na záložku Obecné.
5. Nastavte Množství zboží na „18“.
6. Nastavte položku Chyba v množství na „2“.
7. Do pole Příčina chyby vyberte „Materiál“.
8. Zaškrtněte nebo zrušte zaškrtnutí políčka Koncová práce.
9. Zaškrtněte políčko Akceptovat chybu nebo jeho zaškrtnutí zrušte.
10. Klikněte na tlačítko OK.

## <a name="verify-the-report-as-finished-journal"></a>Ověřte Deník dokončené výroby.
1. V podokně akcí klikněte na možnost Zobrazit.
2. Klepněte na Ohlášeno jako dokončené.
3. Označte v seznamu vybraný řádek.
4. Klikněte na odkaz na vybraném řádku v seznamu.
    * Je zaúčtován Deník dokončené výroby. Podle potřeby můžete v deníku provádět úpravy, můžete ručně vytvořit nový deník, kde můžete provádět změny.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]