---
title: Vytvoření online funkčního profilu
description: Tento článek popisuje, jak vytvořit nový online funkční profil v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 686bc6440c31f3a4d729f2d92e3e57a1cc7b641f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895419"
---
# <a name="create-an-online-functionality-profile"></a>Vytvoření online funkčního profilu

[!include [banner](includes/banner.md)]

Tento článek obsahuje přehled nastavení online funkčních profilů pro Microsoft Dynamics 365 Commerce.

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
  
![Příklad online funkčního profilu.](media/online-functionality-profile.png)

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
