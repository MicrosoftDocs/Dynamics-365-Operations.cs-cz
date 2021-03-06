---
title: Automaticky vytvářené servisní zakázky
description: Servisní zakázky generujete na základě servisních smluv pro platné období servisní smlouvy.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b864aee332c82bc6b6845e7f9e425cfef377033
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824623"
---
# <a name="automatically-create-service-orders"></a>Automaticky vytvářené servisní zakázky 

[!include [banner](../includes/banner.md)]


Servisní zakázky generujete na základě servisních smluv pro platné období servisní smlouvy.

Všechny servisní zakázky, které generujete ze servisní smlouvy, jsou k dané servisní smlouvě přiřazeny.

Servisní objednávky jsou automaticky generovány z následujících nastavení:

  - Jedná se o interval servisní smlouvy nastavený na řádcích servisní smlouvy. Interval servisní smlouvy indikuje frekvenci, s jakou jsou vytvářeny řádky servisní zakázky. Další informace o servisních intervalech naleznete v tématu [servisní intervaly](service-intervals.md).

  - Jedná se o období zadané za účelem definování servisního období v polích **Od data** a **Do data** ve formuláři **Vytvořit servisní zakázky**. Další informace naleznete v tématu [Automatické vytváření servisních zakázek](create-service-orders-automatically.md).

  - Možnost **Kombinovat servisní zakázky** v záhlaví servisní smlouvy. Tato možnost definuje, zda jsou řádky servisní zakázky generovány v servisní smlouvě, a slučuje servisní zakázky podle zaměstnance, servisní úlohy, předmětu servisu nebo servisní smlouvy. Další informace o kombinování servisních zakázek naleznete v tématu [Kombinování servisních zakázek](combine-service-orders.md).

  - Jedná se o možnost **Časové okno** na řádku servisní smlouvy. Dané časové okno definuje, jak daleko lze přesunout řádek servisní zakázky ve vztahu k jeho vypočtenému datu. Další informace naleznete v tématu [Časová okna](time-windows.md)..


> [!NOTE]
> <P>Pokud není den zadaný pro servisní zakázku otevřen v kalendáři vybraném ve formuláři <STRONG>Parametry správy služby</STRONG>, obdržíte zprávu informující o konfliktu kalendáře. Tuto zprávu můžete bezpečně ignorovat a k vytvoření servisní zakázky dojde, přestože je daný den v kalendáři zavřený.</P>

## <a name="example-1"></a>Příklad 1

Servisní smlouva je platná od 1. ledna 2012 až 31. prosince 2012. Pokud servisní období zadané ve formuláři **vytváření servisních zakázek** je od 1. listopad 2012 až 1. února 2013, vytvoří se servisní zakázky od 1. listopad 2012 až 31. prosince 2012.

## <a name="example-2"></a>Příklad 2

Servisní smlouva je platná od 1. ledna 2012 až 31. prosince 2012. K této servisní smlouvě jsou připojeny dva řádky servisní smlouvy. První řádek servisní smlouvy má počáteční datum 2. ledna 2012 a koncové datum 1. března 2012. Druhý řádek servisní smlouvy má počáteční datum 1. dubna 2012 a koncové datum 31. prosince 2012. Můžete určit období ve formuláři **vytváření servisních zakázek** od1. října 2012 do 31. prosince 2012. Servisní zakázky budou tedy generovány pouze pro druhý řádek smlouvy, protože počáteční a koncové datum prvního řádku smlouvy se nachází mimo období zadané pro servisní zakázku.

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]