---
title: Zadání příslušenství dlouhodobého majetku
description: Tento postup popisuje přidání příslušenství k existujícímu dlouhodobému majetku.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetAddition
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc1e13863ae13daaa641f52f7a55e01fc1353dc1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441170"
---
# <a name="enter-an-addition-to-a-fixed-asset"></a>Zadání příslušenství dlouhodobého majetku

[!include [banner](../../includes/banner.md)]

Tento postup popisuje přidání příslušenství k existujícímu dlouhodobému majetku. Účel příslušenství k dlouhodobému majetku je sledování příslušenství, údržby nebo vylepšení majetku, a je pouze informativní. Veškeré změny hodnot nebo životnosti dlouhodobého majetku je nutné provést samostatně.   

Postup využívá účetní role a ukázková data pro právnické osoby USMF.

1. V navigačním podokně přejděte na **Moduly > Dlouhodobý majetek > Dlouhodobý majetek > Dlouhodobý majetek**.
2. V seznamu najděte a vyberte dlouhodobý majetek pro příslušenství.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. V podokně akcí klikněte na možnost **Dlouhodobý majetek**.
5. Klikněte na **Příslušenství dlouhodobého majetku**.
6. Klepněte na možnost **Nový**.
7. Zadejte hodnotu do pole **Název**.
8. V poli **Datum pořízení** nastavte datum nákupu příslušenství nebo služby.
9. V poli **Jednotkové náklady** zadejte cenu položky, údržby nebo jiného zlepšení majetku.
10. Zadejte číslo do pole **Množství**. Celkové náklady nebudou mít vliv na hodnotu dlouhodobého majetku a slouží pouze ke sledování a informačním účelům. Pokud dojde ke kapitalizaci nákladů, je nutné transakce navýšení hodnoty zaúčtovat samostatně.  
11. Klepněte na kartu **Obecné**.

    * Nastavte možnost **Prodlužuje dobu životnosti** na **Ano**, pokud příslušenství prodlužuje dobu životnosti majetku.  
    * Toto pole slouží pouze k informačním účelům. Chcete-li prodloužit dobu životnosti, upravte hodnotu Doba životnosti pro Účetní odpisy a/nebo Knihy odpisů pro majetek.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]