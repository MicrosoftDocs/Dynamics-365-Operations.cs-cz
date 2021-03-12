---
title: Nastavit sklad
description: Toto téma popisuje, jak nastavit sklad, který má být použit s novým kanálem v Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 67c0bb169bee8a7ea90edb4db7233111a8ee6e34
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993646"
---
# <a name="warehouse-set-up"></a>Nastavit sklad


[!include [banner](includes/banner.md)]

Toto téma popisuje, jak nastavit sklad, který má být použit s novým kanálem v Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Ke každému obchodnímu kanálu je nutné přidružit konfigurovaný sklad. Následující postupy poskytují minimální konfiguraci nutnou k nastavení skladu pro obchodní kanál. Další informace týkající se nastavení skladu naleznete v [Přehledu řízení skladu](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json).

## <a name="configure-a-warehouse-site"></a>Konfigurace místa skladu

Před nastavením skladu je nutné nakonfigurovat místo skladu.

Chcete-li konfigurovat místo skladu, postupujte podle následujících kroků.

1. V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Místa**.
1. V podokně akcí zvolte **Nový**.
1. Zadejte hodnotu do pole **Místo**.
1. Zadejte hodnotu do pole **Název**.
1. V části **Obecné** nastavte příslušné **Časové pásmo**.
1. Do sekce **Addresy** zadejte adresu.
1. V podokně akcí vyberte **Uložit**.

Následující obrázek znázorňuje příklad místa skladu.

![Příklad místa skladu](media/warehouse-site.png)

## <a name="set-up-a-warehouse"></a>Nastavit sklad

Chcete-li nastavit sklad, postupujte následujícím způsobem.

1. V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Sklady**.
1. V podokně akcí zvolte **Nový**.
1. V poli **Sklad** zadejte hodnotu.  Pokud se jedná o mapování 1:1 na obchod, zvažte použití názvu obchodu nebo názvu místního distribučního střediska.
1. Zadejte hodnotu do pole **Název**.
1. V rozevíracím seznamu **Místo** vyberte místo skladu, které bylo vytvořeno dříve.
1. V poli **Typ** vyberte **Výchozí**.
    - Chcete-li nastavit **Karanténní sklad**, je nejprve nutné provést následující kroky a vytvořit další sklad, v němž je **Typ** nastaven na **Karanténa**.
    - Chcete-li nastavit **Tranzitní sklad**, je nejprve nutné provést následující kroky a vytvořit další sklad, v němž je **Typ** nastaven na **Tranzitní**.
1. V podokně akcí vyberte **Uložit**.

## <a name="set-up-inventory-aisles"></a>Nastavit skladové uličky

Chcete-li nastavit skladové uličky, postupujte následujícím způsobem.

1. V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Nastavení umístění \> Skladové uličky**.
1. V podokně akcí zvolte **Nový**.
1. V rozevíracím seznamu **Sklad** vyberte místo skladu, které bylo vytvořeno dříve.
1. Do pole **Ulička** zadejte název (například "def").
1. Do pole **Název** zadejte název (například "Výchozí ulička").
1. V podokně akcí vyberte **Uložit**.

## <a name="set-up-warehouse-inventory-locations"></a>Nastavit skladová místa ve skladu

Chcete-li nastavit umístění skladových zásob pro standardní, poškozené a vrácené zásoby, postupujte podle následujících kroků.

1. V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Sklady**.
1. Vyberte dříve vytvořený sklad.
1. V podokně akcí vyberte **Upravit**.
1. V podokně akcí vyberte **Sklad** a pak vyberte **Skladové místo**.
1. V podokně akcí zvolte **Nový**. Rozevírací seznam **Sklad** by měl být výchozí pro váš nový sklad.
    1. Do pole **Ulička** zadejte název uličky, kterou jste zadali dříve. 
    1. Nastavte **Ruční aktualizaci** na **Ano**
    1. Do pole **Umístění** zadejte název skladu.
    1. V podokně akcí vyberte **Uložit**.
 1. V podokně akcí zvolte **Nový**.  Rozevírací seznam **Sklad** by měl být výchozí pro váš nový sklad.
    1. Do pole **Ulička** zadejte název uličky, kterou jste zadali dříve.  
    1. Nastavte **Ruční aktualizaci** na **Ano**
    1. V poli **Umístění** zadejte "Poškozeno".
    1. V podokně akcí vyberte **Uložit**.
 1. V podokně akcí zvolte **Nový**.  Rozevírací seznam **Sklad** by měl být výchozí pro váš nový sklad.
    1. Do pole **Ulička** zadejte název uličky, kterou jste zadali dříve. 
    1. Nastavte **Ruční aktualizaci** na **Ano**
    1. V poli **Umístění** zadejte "Vrácené".
    1. V podokně akcí vyberte **Uložit**.
    
Na následujícím obrázku je znázorněno nastavení skladového místa San Francisco.

![Příklad nastavení skladového místa](media/warehouse-inventory-locations.png)
    
## <a name="complete-warehouse-setup"></a>Dokončené nastavení skladu

Abyste dokončili nastavení skladu, postupujte takto.

1. V navigačním podokně přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Sklady**.
1. Vyberte dříve vytvořený sklad.
1. V podokně akcí vyberte **Upravit**.
1. V **Řízení zásob a skladu**:
    1. Nastavte **Výchozí umístění příjemky** na výchozí místo, které bylo vytvořeno výše.
    1. Vyberte **Výchozí skladové místo výdejů** na výchozí místo, které bylo vytvořeno výše.
1. V části **Adresy** zadejte adresu skladu.
1. V části **Maloobchod**: 
    1. Do pole **Výchozí místo vrácení** zadejte umístění vrácení, které bylo vytvořeno dříve.
    1. Nastavit **Obchod** na **Ano**.
    1. Nastavte **Hmotnost** na **1.00**. 
    1. Do pole **Dimenze úložiště** zadejte výchozí umístění, které bylo vytvořeno dříve.
1. V části **Sklad** nastavte **Záporný fyzický sklad** na **Ano**.
1. V podokně akcí vyberte **Uložit**.

Následující obrázek ukazuje podrobnosti pro konfigurovaný sklad.

![Příklad nakonfigurovaného skladu](media/warehouse-sample.png)

## <a name="additional-resources"></a>Další zdroje

[Přehled řízení skladu](../supply-chain/warehousing/warehouse-management-overview.md?toc=/dynamics365/commerce/toc.json)

[Přehled kanálů](channels-overview.md)

[Předpoklady nastavení kanálu](channels-prerequisites.md)

[Nastavení maloobchodního kanálu](channel-setup-retail.md)
    
[Nastavení online kanálu](channel-setup-online.md)

[Nastavení kanálu kontaktního střediska](channel-setup-callcenter.md)





