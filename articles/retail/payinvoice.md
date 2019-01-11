---
title: "Nastavení scénářů plateb faktur"
description: "Toto téma popisuje, jak nakonfigurovat Dynamics 365 for Retail pro podporu různých scénářů týkajících se plateb faktur."
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: b7132dc9b3c78fa04fcfc38ea72b5678ad08deb2
ms.contentlocale: cs-cz
ms.lasthandoff: 01/04/2019

---
# <a name="set-up-pay-invoice-scenarios"></a>Nastavení scénářů plateb faktur

[!include [banner](includes/banner.md)]

Funkcionalita Platba faktur v aplikaci Dynamics 365 for Retail byla rozšířena, aby podporovala:

- Proplacení vícero faktur prodejní objednávky v jedné transakci POS
- Platba různých typů faktur odběratele, včetně volných faktur, faktur na základě projektu a dobropisů.

Chcete-li povolit tyto scénáře, je třeba nakonfigurovat funkční profil pro obchody podle níže uvedených pokynů.

1. Přejděte na **Maloobchod \> Nastavení kanálu \> Nastavení POS \> Profily POS \> Funkční profily** a zvolte profil, který je navázaný na obchody, u kterých chcete provést změny.
2. Na kartě **Funkce** nakonfigurujte následující parametry podle potřeby.

    - **Faktura prodejní objednávky** - Zvolte **Ano**, čímž povolíte uživateli zaplatit jednu nebo více faktur na základě prodejní objednávky v jedné transakci POS.
    - **Volná faktura** - Zvolte **Ano**, čímž povolíte uživateli zaplatit jednu nebo více volných faktur v jedné transakci POS.
    - **Faktura projektu** - Zvolte **Ano**, čímž povolíte uživateli zaplatit jednu nebo více faktur na základě projektu v jedné transakci POS.
    - **Dobropis prodejní objednávky** - Zvolte **Ano**, čímž povolíte uživateli vyrovnat více dobropisů na základě prodejní objednávky proti otevřeným fakturám nebo zpracovat refundaci zákazníkovi pro otevřený dobropis.

> [!NOTE]
> Platba nebo vyrovnání dílčích částek není ještě podporována.

