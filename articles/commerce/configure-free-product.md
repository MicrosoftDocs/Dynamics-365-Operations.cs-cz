---
title: Konfigurace produktu, který bude zakoupen zdarma
description: Tento článek popisuje, jak nakonfigurovat produkt tak, aby jej bylo možné zakoupit zdarma, v Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 88370085de047a5e0be773dde218770cfa242d14
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280357"
---
# <a name="configure-a-product-to-be-purchased-for-free"></a>Konfigurace produktu, který bude zakoupen zdarma

[!include [banner](includes/banner.md)]


Tento článek popisuje, jak nakonfigurovat produkt tak, aby jej bylo možné zakoupit zdarma, v Microsoft Dynamics 365 Commerce.

## <a name="configure-the-product"></a>Konfigurace produktu

Chcete-li prodat produkt zdarma v Dynamics 365 Commerce, musíte nastavit jeho cenu na 0 (nulu). Kromě toho musíte nakonfigurovat nastavení produktu **Nulová cena platí**.

Ke konfiguraci nastavení **Nulová cena platí** v centrále Commerce postupujte následovně.

1. Přejděte do nabídky **Retail a Commerce \> Produkty a kategorie \> Uvolněné produkty podle kategorie**.
1. Přejděte na produkt, který chcete prodat zdarma. 
1. V části **Commerce** stránky produktu nastavte možnost **Nulová cena platí** na **Ano**.

Následující obrázek ukazuje příklad produktu, kde je možnost **Nulová cena platí** nastavena na **Ano**.

![Příklad produktu, kde je možnost Nulová platná cena nastavena na Ano.](./media/Zero-price.png)

## <a name="configure-the-online-stores-functionality-profile"></a>Nakonfigurujte funkční profil internetového obchodu

Před zpracováním bezplatných transakcí byste měli nakonfigurovat nastavení **Povolit pokladnu bez plateb** profilu funkčnosti vašeho internetového obchodu tak, aby byly povoleny transakce, které nemají žádné platby. Informace o tom, jak vytvořit funkční profily, viz [Vytvoření online funkčního profilu](online-functionality-profile.md).

Ke konfiguraci nastavení **Povolit pokladnu bez plateb** v centrále Commerce postupujte následovně.

1. Přejděte na **Retail a Commerce \> Nastavení kanálu \> Nastavení online obchodu**.
1. Na stránce funkčního profilu vašeho obchodu pod **Pokladna**, nastavte možnost **Povolit pokladnu bez plateb** na **Ano**.

Následující obrázek ukazuje příklad profilu internetového obchodu, kde je možnost **Povolit pokladnu bez plateb** nastavena na **Ano**.

![Příklad profilu internetového obchodu, kde je možnost Povolit pokladnu bez plateb nastavena na Ano.](./media/Zero-price-profile.png)

## <a name="additional-resources"></a>Další prostředky

[Správa maloobchodní prodejní ceny](price-management.md)

[Vytvoření online funkčního profilu](online-functionality-profile.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
