---
title: Vyrovnání zůstatku
description: Částku zbývající z aktivity vyrovnání můžete vyrovnat použitím částky na účet hlavní knihy.
author: mikefalkner
ms.date: 10/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8c865b4b0481b7753588ef17bc0250bab2b6c191
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834906"
---
# <a name="settle-remainder"></a>Vyrovnání zůstatku

[!include [banner](../includes/banner.md)]

Částku zbývající z aktivity vyrovnání můžete vyrovnat použitím částky na účet hlavní knihy nebo jiného zákazníka. Zůstatek můžete vyrovnat, když vyrvnáváte částky zadané do deníku nebo když vyrovnáváte pouze otevřené transakce.

## <a name="setting-up-defaults"></a>Nastavení výchozího nastavení 
Musíte povolit funkci Vyrovnat zůstatek a zadat výchozí nastavení, než použijete funkci Vyrovnat zůstatek

1)  Klepněte na tlačítko **Pohledávky > Parametry > vyrovnání** nebo **Závazky > Parametry > vyrovnání**
2)  Vyberte záložku **Vyrovnání** a klepněte na tlačítko **Povolit vyrovnání zůstatku**
3)  V části **Výchozí kód důvodu** vyberte výchozí kód důvodu. Kódy důvodu musí být již nastaveny v umístění **Pohledávky > Nastavení > Kódy důvodu odpisu odběratele** nebo **Závazky > Nastavení > Kódy důvodu odpisu odběratele**. **Výchozí účet pro vyrovnání zůstatku** bude přednastaven na účet přiřazený k tomuto kódu důvodu odpisu.
3)  Aktualizujte **Výchozí účet pro vyrovnání zůstatku** podle potřeby.
4)  V poli **Výchozí název deníku** vyberte deník platby, který bude použit, pokud chcete vytvořit deník plateb, když nastavujete pouze otevřené transakce. Pokud aktivujete funkci vyrovnat zůstatek, je nutné přidat výchozí název deníku.

## <a name="settle-remainder-from-a-journal"></a>Vyrovnat zůstatek z deníku
Pokud nepovolíte funkci **Vyrovnat zůstatek**, můžete stále zadávat transakce do deníku a poté proti němu vyrovnat transakce, jak jste to dělali v minulosti. Po klepnutí na tlačítko **OK** bude otevřený zůstatek na faktuře snížen o peněžní částku. Pokud hotovost zcela nevyrovná fakturu, faktura je ponechána se zbývající částkou k vyrovnání později.

Pokud je funkce **Vyrovnat zůstatek** povolena, můžete vyrovnat zbývající částku na účet hlavní knihy. Zbývající částku lze také převést na další účet odběratele (pro transakce odběratelů) nebo dodavatele (pro transakce dodavatele) namísto toho, abyste faktury ponechali otevřené. 

Chcete-li vyrovnat zůstatek ze stránky **Vyrovnání**, proveďte následující kroky:

1)  Na stránce **Vyrovnání** označte faktury nebo transakce, které chcete vyrovnat.
2)  Klepněte tlačítko **Vyrovnat zůstatek**.
3)  Zobrazí se dialogové okno zobrazující částku, která bude vyrovnána oproti účtu hlavní knihy, datum, které bude použito k vyrovnání zbývající částky, výchozí kód důvodu z parametrů a výchozí účet z parametrů. 
4)  Vyberte důvod nového vyrovnání, pokud si přejete změnit výchozí důvod. Účet vyrovnání se změní na účet související s kódem důvodu.
5)  Upravte účet vyrovnání, pokud jej chcete změnit.
6)  Pokud vyrovnáváte transakce odběratele a chcete, aby byla zbývající částka přesunuta jinému odběrateli, vyberte zákazníka v poli **Vyrovnání zůstatku proti účtu odběratele**. Pokud vyrovnáváte transakce dodavatele a chcete, aby byla zbývající částka přesunuta jinému dodavateli, vyberte dodavatele v poli **Vyrovnání zůstatku proti účtu dodavatele**.
6)  Klikněte na **Vyrovnat zůstatek**.
7)  Zobrazí se stránka **Deník**. Do deníku bude přidán další řádek deníku se zbývající částkou vyrovnání a s účtem vyrovnání zůstatku jako protiúčtem. Pokud jste přidali odběratele nebo dodavatele, abyste mohli přesunout částku vyrovnání na jiného odběratele nebo dodavatele, do deníku bude přidán další řádek pro přesun částky vyrovnání danému odběrateli nebo dodavateli.

Při zaúčtování deníku bude otevřená transakce zcela vyrovnána. 

## <a name="settle-remainder-when-you-are-only-settling-open-transactions"></a>Vyrovnat zůstatek, když vyrovnáváte pouze otevřené transakce
Zbývající částku můžete také vyrovnat, když vyrovnáváte otevřené transakce bez deníku.

Pro vyrovnání zbývající částky proveďte následující kroky:

1)  Na stránce **Vyrovnání** označte faktury nebo transakce, které chcete vyrovnat.
2)  Klikněte na **Vyrovnat zůstatek**.
3)  Zobrazí se dialogové okno zobrazující částku, která bude vyrovnána oproti účtu hlavní knihy, datum, které bude použito k vyrovnání zbývající částky, výchozí kód důvodu z parametrů a výchozí účet z parametrů. 
4)  Vyberte důvod nového vyrovnání, pokud si přejete změnit výchozí důvod. Účet vyrovnání se změní na účet související s kódem důvodu.
5)  Upravte **účet vyrovnání**, pokud jej chcete změnit.
6)  Pokud vyrovnáváte transakce odběratele a chcete, aby byla zbývající částka přesunuta jinému odběrateli, vyberte zákazníka v poli **Vyrovnání zůstatku proti účtu odběratele**. Pokud vyrovnáváte transakce dodavatele a chcete, aby byla zbývající částka přesunuta jinému dodavateli, vyberte dodavatele v poli **Vyrovnání zůstatku proti účtu dodavatele**
7)  Můžete také vytvořit deník plateb se zbývající částkou vyrovnání nebo ji zaúčtovat bez deníku. Vyberte **Ano** pro **Upravit v deníku** pro vytvoření deníku plateb. Budete moci upravit deník plateb, který vytvoříte.
8)  Klikněte na **Vyrovnat zůstatek**. Pokud chcete vytvořit deník, tlačítko se změní na **Vytvořit deník**. Namísto toho klikněte na **Vytvořit deník**.
9)  Jestliže jste vytvořili deník plateb, stránka deníku se otevře po klepnutí na tlačítko **Vyrovnání zůstatku**. Do deníku bude přidán řádek deníku se zbývající částkou vyrovnání a s účtem vyrovnání zůstatku jako protiúčtem. Pokud jste přidali odběratele nebo dodavatele, abyste mohli přesunout částku vyrovnání na jiného odběratele nebo dodavatele, do deníku bude přidán další řádek pro přesun částky vyrovnání danému odběrateli nebo dodavateli.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]