---
title: Vytvoření funkčního profilu maloobchodu
description: Toto téma popisuje, jak vytvořit nový funkční profil v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 14da5fd2b409790de2269036ccb941ffa6d3311c
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478301"
---
# <a name="create-a-retail-functionality-profile"></a>Vytvoření funkčního profilu maloobchodu

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak vytvořit nový funkční profil v řešení Microsoft Dynamics 365 Commerce.

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
  
![Příklad funkčního profilu](media/retail-functionality-profile.png)

## <a name="additional-resources"></a>Další zdroje

[Informační kódy a skupiny informačních kódů](info-codes-retail.md)           

[Vytvoření nového adresáře](new-address-book.md) 

[Přehled rozložení obrazovky](pos-screen-layouts.md)       

[Konfigurace a instalace Retail hardware station](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
