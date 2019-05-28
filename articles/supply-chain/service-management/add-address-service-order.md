---
title: Přidání adresy do servisní zakázky
description: Toto téma popisuje postup přidání adresy odběratele do servisní zakázky.
author: ShylaThompson
manager: AnnBe
ms.date: 05/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58188be6f82b6587011188379e5370b81f8fd114
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570358"
---
# <a name="add-an-address-to-a-service-order"></a>Přidání adresy do servisní zakázky    

[!include [banner](../includes/banner.md)]


Toto téma popisuje postup přidání adresy odběratele do servisní zakázky. Při vytváření servisní zakázky se informace o adrese přenáší z projektu, ke kterému je servisní zakázka připojena. Pro odběratele, dodavatele, pracoviště, sklady, servisní zakázky a projekty však můžete vybrat alternativní umístění z adres, které jsou již zadány v aplikaci Microsoft Dynamics AX.

Můžete také vytvořit adresy nové. Ve výchozím stavu je nová adresa převedena do projektu. Můžete však zadat, aby nová adresa byla relevantní pouze pro tuto instanci služby. V takovém případě nová adresa do projektu převedena nebude.

## <a name="create-a-customer-address-for-a-service-order"></a>Vytvoření adresy zákazníka pro servisní zakázku

Pro přidání adresy do servisní zakázky postupujte takto:

1.  Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.

2.  Otevřete servisní zakázku, pro kterou chcete vytvořit adresu.

3.  V **podokně akcí** klepněte na tlačítko **Upravit** a klepněte na možnost **Zobrazení záhlaví**.

4.  Na pevné záložce **adresy** klepněte na tlačítko **přidání adresy**.

5.  Ve formuláři **Nová adresa** zadejte jedinečný název adresy a vyplňte zbývající pole. 
    

    > [!WARNING]
    > <P>Zadáte-li stejný název, jaký používá existující adresa, informace zadané do zbývajících polí přepíší informace pro existující adresu.</P>


6.  Klepnutím na tlačítko **OK** zkopírujete novou adresu do servisní zakázky.

## <a name="specify-an-alternative-address-on-a-service-order"></a>Zadání alternativní adresy pro servisní zakázku

Pro přidání alternativní adresy do servisní zakázky postupujte takto:

1.  Klikněte na uzel **Řízení služeb** \> **Společné** \> **Servisní zakázky** \> **Servisní zakázky**.

2.  Otevřete servisní zakázku, pro kterou chcete zadat alternativní adresu.

3.  V **podokně akcí** klepněte na tlačítko **Upravit** a klepněte na možnost **Zobrazení záhlaví**.

4.  Na pevné záložce **adresy** klepněte na tlačítko **Jiná adresa**.

5.  Ve formuláři **výběr adresy** v poli **typ záznamu** vyberte **servisní zakázky**.

6.  Vyberte adresu a klepnutím na tlačítko **OK** ji zkopírujete do servisní zakázky.


  


