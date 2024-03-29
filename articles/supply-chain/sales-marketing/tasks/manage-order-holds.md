---
title: Správa blokování objednávek
description: Tento postup ukazuje, jak blokovat prodejní objednávky odběratele, jak pracovat s rezervacemi blokovaných objednávek a jak odebrat blokování objednávky.
author: Henrikan
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 938b21b66b7b61452be104936877278a3bc120f2
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566285"
---
# <a name="manage-order-holds"></a>Správa blokování objednávek

[!include [banner](../../includes/banner.md)]

Tento postup ukazuje, jak blokovat prodejní objednávky odběratele, jak pracovat s rezervacemi blokovaných objednávek a jak odebrat blokování objednávky. Objednávka může být blokována z mnoha důvodů. Můžete například blokovat objednávku, dokud není ověřena adresa odběratele nebo platební metoda nebo dokud správce nezkontroluje úvěrový limit odběratele. Když je objednávka blokována, nelze ji zpracovat skladem pro expedici. 

Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="set-up-order-holds"></a>Nastavení blokování objednávky
1. Přejděte na **Navigační podokno > Moduly > Prodej a marketing > Nastavení > Prodejní objednávky > Kódy blokování objednávky**.
2. Klepněte na možnost **Nový**.
3. V poli **Kód blokování** zadejte hodnotu. Zadejte například Zpětné volání.  
4. Zadejte hodnotu do pole **Popis**.
    - Například blokovaná objednávka čekající na zpětné volání odběratele.  
    - Volitelně zaškrtněte políčko **Odebrat rezervace**, abyste odstranili všechny fyzické rezervace z objednávky, když je přidán kód blokování.  
5. Klikněte na možnost **Uložit**.

## <a name="place-order-on-hold"></a>Zablokování objednávky
1. Přejděte na **Navigační podokno > Moduly > Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky**.
2. Klepněte na možnost **Nový**.
3. V poli **Účet odběratele** zadejte nebo vyberte hodnotu.
4. Klikněte na tlačítko **OK**.
5. V poli **Číslo položky** zadejte nebo vyberte hodnotu.
6. Zadejte číslo do pole **Množství**.
7. V **podokně akcí** klikněte na možnost **Prodejní objednávka**.
8. Klikněte na **Blokování objednávky**.
9. Klepněte na možnost **Nový**.
10. V poli **Kód blokování** vyberte kód, který jste vytvořili v předchozím dílčím úkolu.
11. Klikněte na možnost **Uložit**.
12. Zavřete stránku.
13. Přejděte na **Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky**.
14. Označte v seznamu vybraný řádek. Objednávky, které jsou aktuálně blokovány, mají označena pole „Nezpracovávat a „Blokace“.
15. V podokně akcí klikněte na tlačítko **Vyskladnit a zabalit**.

## <a name="manage-order-holds"></a>Správa blokování objednávek
1. Přejděte na **Prodej a marketing > Prodejní objednávky > Otevřené objednávky > Blokování objednávky**. Stránka s **blokovanými objednávkami** funguje jako pracovní plocha, kde můžete získat přehled všech aktuálních a zpracovaných blokování, se kterými zde můžete pracovat, a přidružených prodejních objednávek.     
2. Označte v seznamu vybraný řádek.
3. V **podokně akcí** klikněte na **Rezervace blokování**.
4. Klikněte na možnost **Rezervace**.
5. Odznačte vybraný řádek na seznamu. Pole **Rezervovat komu** nyní zobrazuje vaše uživatelské ID.   
6. Klikněte na možnost **Vymazat rezervaci**.
7. V **podokně akcí** klikněte na možnost **Vymazat blokování**.
    - Když jste připraveni odebrat blokování a umožnit objednávce, aby pokračovala k dalšímu kroku plnění, musíte blokování vymazat. Nevyžaduje-li objednávka žádné změny, můžete spustit akci Vymazat blokování. Můžete však použít akci Vymazat a upravit, pokud je třeba při vymazání blokování objednávku aktualizovat.      
    - Akce **Vymazat a odeslat** je použitelná pouze při použití funkce kontaktního střediska.  
8. Klikněte na možnost **Vymazat blokování**. Blokování nyní bylo z objednávky vymazáno a odebráno ze seznamu aktivních blokací. Všechna blokování a jejich podmnožinu podle specifického stavu zobrazíte změnou hodnoty v poli Zobrazit.     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]