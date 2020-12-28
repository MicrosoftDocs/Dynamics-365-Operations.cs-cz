---
title: Vytvoření online funkčního profilu
description: Toto téma popisuje, jak vytvořit nový online funkční profil v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5ecbfcf3fa78ad2909a7cc9988ab1edaf2b98376
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410905"
---
# <a name="create-an-online-functionality-profile"></a>Vytvoření online funkčního profilu


[!include [banner](includes/banner.md)]

Toto téma obsahuje přehled nastavení online funkčních profilů pro Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Profil online funkcí poskytuje různá nastavení používaná pro online kanály. Každý online kanál musí určovat profil online funkcí.

## <a name="create-an-online-functionality-profile"></a>Vytvoření online funkčního profilu

Následující postup vysvětluje, jak vytvořit online profil funkcí z aplikace Commerce Headquarters.

1. V navigačním podokně přejděte na **Moduly \> Nastavení kanálu \> Nastavení online obchodu \> Profily funkcí**.
1. V podokně akcí zvolte **Nový**.
1. V poli **Profil** zadejte ID profilu.
1. Do pole **popis** zadejte hodnotu ("profil Adventure Works" v následujícím příkladu obrázku).
1. V části **Funkce** upravte podle potřeby nastavení **KOšíK**, **ZáKAZNíCI MALOOBCHODU** nebo **POKLADNA**.
1. V podokně akcí vyberte **Uložit**.

Následující obrázek znázorňuje příklad online funkčního profilu.
  
![Příklad online funkčního profilu](media/online-functionality-profile.png)

## <a name="functions"></a>Funkce

- **Agregované produkty** Pokud je tato funkce povolena, umožňuje košíku aktualizovat množství při vícenásobném přidání stejné položky.
- **Povolit rezervaci bez plateb**: Pokud je tato funkce povolena, zpracuje scénář, kdy položky přidané do vozíku mají cenu 0.00 USD.
- **Vytvořit odběratele v asynchronním režimu**: Toto nastavení je zastaralé pro kanály elektronického obchodu třetí strany a není použitelné pro web Dynamics 365 e-Commerce.

## <a name="additional-resources"></a>Další zdroje

[Přehled kanálů](channels-overview.md)

[Předpoklady nastavení kanálu](channels-prerequisites.md)

[Nastavení online kanálu](channel-setup-online.md)

[Nastavení maloobchodního kanálu](channel-setup-retail.md)

[Nastavení kanálu kontaktního střediska](channel-setup-callcenter.md)
