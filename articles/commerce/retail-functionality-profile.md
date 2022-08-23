---
title: Vytvoření funkčního profilu maloobchodu
description: Tento článek popisuje, jak vytvořit nový funkční profil v řešení Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: f006aaf594f1df097f80c77794e34f9b831e9949
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280234"
---
# <a name="create-a-retail-functionality-profile"></a>Vytvoření funkčního profilu maloobchodu

[!include [banner](includes/banner.md)]

Tento článek popisuje, jak vytvořit nový funkční profil v řešení Microsoft Dynamics 365 Commerce.

Funkční profil Commerce poskytuje různá nastavení používaná pro online kanály. Každý kanál musí určovat funkční profil.

## <a name="create-a-functionality-profile"></a>Vytvořit funkční profil

Při vytváření nového funkčního profilu postupujte takto.

1. V navigačním podokně přejděte na **Moduly \> Nastavení kanálu \> Profily POS \> Profily funkcí**.
1. V podokně akcí zvolte **Nový**.
1. V poli **Profil** zadejte ID profilu ("FN006" v níže uvedeném příkladu obrázku).
1. Do pole **popis** zadejte hodnotu ("profil Adventure Works" v následujícím příkladu obrázku).
1. V části **obecné** vyberte zemi pro národní prostředí **ISO**.
1. V části **Obecné** upravte podle potřeby další nastavení.
1. V části **Obecné** vyberte **ID profilu účtenky** pro příjem e-mailů.
1. V části **Funkce** upravte podle potřeby další nastavení.
1. V části **částka** upravte podle potřeby další nastavení.
1. V části **Informační kódy** upravte podle potřeby další nastavení.
1. V části **Číslování příjmu** upravte podle potřeby další nastavení. 
  
Následující obrázek znázorňuje příklad funkčního profilu.
  
![Příklad funkčního profilu.](media/retail-functionality-profile.png)

## <a name="additional-resources"></a>Další prostředky

[Informační kódy a skupiny informačních kódů](info-codes-retail.md)           

[Vytvoření nového adresáře](new-address-book.md) 

[Přehled rozložení obrazovky](pos-screen-layouts.md)       

[Konfigurace a instalace Retail hardware station](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
