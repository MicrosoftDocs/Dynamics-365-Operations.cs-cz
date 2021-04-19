---
title: Kontrola dostupnosti zásob
description: Tento postup popisuje způsob kontroly množství na skladě a zásob fyzicky k dispozici pro určité číslo položky.
author: ShylaThompson
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventOnHandItemListPage, SysQueryForm, InventDimParmFixed, InventSupply, DefaultDashboard, WHSInventPhysicalOnhand, WHSOnHand, InventOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1b68a40ba433f7db6eb910961cd429629387bbe
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834090"
---
# <a name="check-the-availability-of-stock"></a>Kontrola dostupnosti zásob

[!include [banner](../../includes/banner.md)]

Tento postup popisuje způsob kontroly množství na skladě a zásob fyzicky k dispozici pro určité číslo položky. Také ukazuje, jak získat informace o zásobách související s položkou. Fyzické zásoby na skladě je množství na skladě, které je k dispozici – tedy, je zakoupené, přijaté a registrované. Množství na skladě zahrnuje dostupné zásoby na skladě, ale i zásoby, které byly objednány a jsou očekávané, ale dosud nebyly přijaty nebo registrovány. Tento proces můžete projít pomocí ukázkových dat společnosti USMF nebo pomocí vlastních dat. Pokud používáte USMF, můžete použít ukázkové hodnoty, které jsou zobrazeny. Tyto úkoly obvykle provádějí pracovníci skladu.


## <a name="check-on-hand-inventory-for-an-item"></a>Kontrola zásob na skladě pro konkrétní položku
1. Přejděte na **Navigační podokno > Moduly > Řízení zásob > Dotazy a sestavy > Zásoby na skladě**.
2. Vyberte řádek **Číslo položky**. Pokud chcete vytvořit dotaz na množství na skladě podle čísla položky, vyberte řádek, kde je Tabulka nastavena na **Množství na skladě**, a Pole je nastaveno na číslo **Položky**.
3. V poli **Kritéria** vyberte položku, pro kterou chcete vytvořit dotaz. V případě, že používáte ukázková data společnosti USMF, můžete vybrat 'M9201'.  
4. Klikněte na tlačítko **OK**.
5. V **podokně akcí** klikněte na možnost **Dimenze**. Karta **Dimenze** umožňuje vybrat způsob, jak podrobné údaje chcete zobrazit o množství na skladě. Pokud potřebujete data související s rezervací, musíte zobrazit všechny dimenze zásob pro položky používající procesy rozšířené skladu (řízení skladu).
6. Klikněte na tlačítko **OK**.
7. V **podokně akcí** klikněte na možnost **Související informace**. Pokud tuto možnost nevidíte, klikněte na tlačítko se třemi tečkami (...) a otevřete tak další možnosti v podokně.
8. Klikněte na **Přehled dodávek**. Karta **Přehled dodávek** obsahuje informace o zásobách pro určitou položku, jako je například množství na skladě, doba realizace a informace o dodavateli.  
9. Rozbalte sekci **Na skladě**.
10. Rozbalte sekci **Dodavatelé**.
11. Zavřete stránku.
12. Zavřete stránku.

## <a name="check-physical-on-hand-inventory"></a>Kontrola fyzického množství na skladě
1. Přejděte na **Navigační podokno > Moduly > Řízení skladu > Dotazy a sestavy > Fyzické zásoby na skladě**.
2. Zadejte hodnotu do pole **Číslo zboží**. Chcete-li filtrovat seznam položek, můžete použít pole Pracoviště a Sklad. 
3. Aktualizujte stránku.
4. V **podokně akcí** klikněte na možnost **Zobrazit dimenze**. Karta Zobrazit dimenze umožňuje vybrat způsob, jak podrobné údaje chcete zobrazit o množství na skladě.
5. Klikněte na tlačítko **OK**.
6. Zavřete stránku.

## <a name="check-on-hand-inventory-by-location"></a>Kontrola množství na skladě podle skladového místa
1. Přejděte na **Navigační podokno > Moduly > Řízení skladu > Dotazy a sestavy > Množství na skladě podle místa**.
2. Zadejte hodnotu do pole **Sklad**. V případě, že používáte ukázková data společnosti USMF, můžete použít „51“.  
3. Aktualizujte stránku.
4. Klikněte na **Zobrazit dimenze**.
5. Klikněte na tlačítko **OK**.
6. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]