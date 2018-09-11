--- 
title: "Stanovení platebních poplatků odběratele"
description: "Vytvořte poplatky pro platbu pro úhrady odběratelů."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPaymFee, CustPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 659f4560747cea73c61a9b748a980946ca252bd6
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="establish-customer-payment-fees"></a>Stanovení platebních poplatků odběratele

[!include [task guide banner](../../includes/task-guide-banner.md)]

Vytvořte poplatky pro platbu pro úhrady odběratelů.

Tento úkol používá ukázkovou společnost USMF.

1. Přejděte do nabídky Pohledávky > Nastavení platby > Platební poplatek.
2. Klikněte na položku Nová.
3. V poli ID poplatku zadejte ID poplatku.
    * ID poplatku se zobrazí na denících platby, takže je zadejte dostatečně popisné, aby bylo možné pochopit, jaký poplatek je vyměřen.  
4. Do pole Název zadejte název poplatku.
5. Do pole Popis poplatku zadejte popis poplatku.
6. Určete, zda poplatek bude účtován z účtu hlavní knihy nebo odběratele.
    * Pokud je odběrateli stanoven poplatek, vyberte Odběratel. Pokud bude poplatek vyměřen pro vaši organizaci v rámci výdajů, vyberte Hlavní kniha. Pro tento úkol vyberte Odběratele.  
7. Vyberte typ deníku, který lze použít pro tento platební poplatek.
    * Pokud se tyto poplatky používají pro platby odběratelů, typu deníku bude pravděpodobně Platba odběratele.  
8. Klikněte na položku Uložit.
9. Klikněte na Nastavení platebního poplatku.
    * Nastavení platebního poplatku se používá ke stanovení kritérií pro dobu, kdy se platebního poplatek hodnotí.  Můžete například definovat, že bude poplatek vypočítán, pokud je bankovní účet USMF OPER, a způsob platby je šek.  
10. Zaškrtněte buď Tabulka, Skupina nebo Vše a definujte tak, jaké bankovní účty, budou oceněny pro tento poplatek.
    * Pokud vyberete možnost Vše, všechny bankovní účty mohou hodnotit tento poplatek.  Pokud vyberete Tabulka, může být pro tento poplatek hodnocen pouze vybraný bankovní účet. Jestliže vyberete Skupina, pouze bankovní účty ve vybrané bankovní skupině mohou být vyhodnoceny pro tento poplatek.  
11. Vyberte bankovní účet nebo bankovní skupinu.
    * Pokud vyberete Tabulka, zobrazí se vyhledávání bankovních účtů. Pokud vyberete Skupina, zobrazí se vyhledávání bankovních skupin.  
12. Klikněte na odkaz na vybraném řádku v seznamu.
13. Vyberte metodu platby, pro kterou se vyhodnotí tento poplatek.
    * Můžete například vyhodnotit poplatek pro vaše odběratele, jestliže odešlou platby jako šek, nikoli jako elektronickou platbu.  
14. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
15. V případě potřeby zadejte měnu platby.
    * Měna platby se používá jako další kritérium pro to, zda budou poplatky posouzeny.  Například může vaše banka účtovat dodatečný poplatek pro plateb přijaté v měně USD, protože obvykle provádí pouze transakce v měně EUR.  
16. Určete, zda poplatek budou procenta, částka nebo interval.
17. Zadejte procento nebo částku poplatku.
    * Je-li v poli Procento/Částka vybrána možnost Procento, pak hodnota zadaná zde bude procento. Je-li v poli Procento/Částka vybrána možnost Částka, pak hodnota zadaná zde bude částka. Je-li v poli Procento/Částka vybrána možnost Interval, použijte kartu Interval pro definování úrovní.  
18. V poli Měna poplatku vyberte měny poplatku.
    * Toto je měna, v níž bude vytvořen poplatek.  
19. Klikněte na položku Uložit.


