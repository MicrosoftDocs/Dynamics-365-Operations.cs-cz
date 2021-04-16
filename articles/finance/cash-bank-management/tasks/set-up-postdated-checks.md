---
title: Nastavení postdatovaných šeků
description: Toto téma vysvětluje, jak určit, zda se mají zaúčtovat položky deníku pro postdatované šeky a které účetní deníky se mají použít pro vymazání položek a plateb dodavatele.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2adb8b969a6e86becaa3c0a3b59d8f8f259e5a64
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834589"
---
# <a name="set-up-postdated-checks"></a>Nastavení postdatovaných šeků

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak určit, zda se mají zaúčtovat položky deníku pro postdatované šeky a které účetní deníky se mají použít pro vymazání položek a plateb dodavatele. Můžete také určit clearingové účty pro vydané šeky, přijaté šeky a srážkové daně. Postdatované šeky jsou vydány za účelem provedení a přijetí platby v budoucí datu. Můžete zadat, zda se má šek odrazit ve vašich účetních knihách před datem splatnosti.



Role tohoto postupu je Pokladník. Tato procedura používá ukázkovou společnost USMF.


## <a name="set-up-postdated-checks"></a>Nastavení postdatovaných šeků
1. Přejděte do nabídky Pokladna a banka > Nastavení > Parametry pokladny a banky.
2. Klikněte na kartu Postdatované šeky.
3. Zaškrtněte políčko Povolit postdatované šeky nebo jeho zaškrtnutí zrušte.
4. Zaškrtněte políčko Zaúčtovat položky deníku pro postdatované šeky nebo jeho zaškrtnutí zrušte.
5. V poli Clearingový účet pro vydané šeky zadejte požadované hodnoty.
6. V poli Clearingový účet pro přijaté šeky zadejte požadované hodnoty.
7. V poli Hlavní deník pro položky clearingu zadejte hodnotu.
8. V poli Přenést postdatované šeky do tohoto deníku plateb dodavatelů zadejte hodnotu.
9. Zadejte požadované hodnoty do pole Clearingový účet srážkové daně.
10. Klikněte na položku Uložit.
11. Zavřete stránku.
12. Přejděte do nabídky Závazky > Nastavení platby > Metody platby.
13. Klikněte na položku Nová.
14. V poli Způsob platby zadejte hodnotu.
15. Zvolením možnosti Clearingové zaúčtování postdatovaných šeků určete, že je částka šeku zaúčtována na clearingový účet.
16. V poli Typ účtu vyberte „Banka“.
    * Pole pro protiúčet způsobu platby bude prázdné.  
17. Zadejte požadované hodnoty do pole Platební účet.
    * Vyberte bankovní účet, který se používá k odečtu částky faktury.  
18. Klepněte na tlačítko Uložit.
19. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]