---
title: Vytvoření nového rozvržení skladu
description: Tento článek popisuje, jak nastavit informace o umístění ve skladu.
author: yufeihuang
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143648e5317e6dce1b1a76a96d6069abe5d0e351
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859307"
---
# <a name="create-a-new-warehouse-layout"></a>Vytvoření nového rozvržení skladu

[!include [banner](../../includes/banner.md)]

Tento článek popisuje, jak nastavit informace o umístění ve skladu. To platí pouze pro sklady vytvořené pomocí "základních funkcí skladu" v modulu Řízení zásob, ne pro sklady, které jsou vytvořeny v modulu Řízení skladu. Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.


## <a name="set-the-default-location-capacity"></a>Nastavte výchozí kapacitu skladového místa
1. V navigačním podokně přejděte na **Moduly > Řízení zásob > Nastavení > Parametry řízení zásob a skladu**.
2. Vyberte karu **Umístění**.
3. V poli **Standardní šířka** zadejte číslo.
4. V poli **Standardní hloubka** zadejte číslo.
5. V poli **Standardní výška** zadejte číslo.
6. Zvolte **Uložit**.
7. Zavřete stránku.

## <a name="define-the-location-name-format"></a>Definujte formát názvu skladového místa
1. V navigačním podokně přejděte na **Moduly > Řízení zásob > Nastavení > Rozdělení zásob > Sklady**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Sklad**.
4. Zadejte hodnotu do pole **Název**.
5. V poli **Pracoviště** vyberte požadovaný záznam ve vyhledávání.
6. Přepněte rozšíření oddílu **Názvy umístění**. Možnosti v tomto oddílu definují výchozí formát pro názvy umístění. V našem příkladu použijeme čísla uličky, stojanu a police.  
7. Nastavte možnost **Včetně uličky** na **Ano**.
8. Nastavte možnost **Včetně stojanu** na **Ano**. 
9. V poli **Formát** zadejte hodnotu pro stojan.
10. Nastavte možnost **Včetně police** na **Ano**.
11. V poli **Formát** zadejte pro polici hodnotu.

## <a name="define-warehouse-locations"></a>Definujte umístění ve skladu
1. V podokně akcí zvolte **Sklady**.
2. Zvolte **Průvodce skladovým místem**.
3. Zvolte **Další**.
4. Zrušte výběr možnosti **Výstupní překladiště**
5. Zrušte výběr možnosti **Hromadné umístění**
6. Vyberte **Další**, dokud nepřejdete na možnost **Dokončit**.
7. Zavřete stránku.
8. Aktualizujte stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]