---
title: Vrácení produktů řízených sériovým číslem v POS
description: Tento článek popisuje možnosti pro ověřování serializovaných položek jako součást procesu vrácení v aplikaci Microsoft Dynamics 365 Commerce Point of Sale (POS).
author: hhainesms
ms.date: 06/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 9fa7e47b6d650370afe4b98d7eca01253bd1bc36
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268467"
---
# <a name="return-serial-numbercontrolled-products-in-pos"></a>Vrácení produktů řízených sériovým číslem v POS

[!include [banner](includes/banner.md)]

Tento článek popisuje možnosti pro ověřování serializovaných položek jako součást procesu vrácení v aplikaci Microsoft Dynamics 365 Commerce Point of Sale (POS).

> [!NOTE]
> Ve verzi Commerce verze 10.0.20 a novějších je k dispozici nová funkce s názvem **Sjednocené prostředí pro zpracování vrácení v POS**. Chcete-li během zpracování vratky objednávky v POS použít ověření sériového čísla, musíte tuto funkci zapnout. Informace o dalších schopnostech, které tato funkce poskytuje, když je zapnutá, najdete v tématu [Vytvoření vrácení v POS](POS-returns.md).
>
> Poté, co funkci zapnete, ji nelze vypnout.

## <a name="options-for-validating-serialized-returns"></a>Možnosti pro ověření serializovaných vratek

Když je funkce **Sjednocené prostředí pro zpracování vrácení v POS** zapnutá, mohou organizace provádět ověření vracených položek řízených sériovým číslem prostřednictvím POS. Tato funkce může varovat uživatele, pokud se vracené sériové číslo liší od původního sériového čísla, které bylo prodáno. Ve verzi Commerce verze 10.0.20 a novějších je zpráva, kterou uživatelé obdrží, pouze varovnou zprávou. Uživatelé mohou pokračovat ve zpracování vratky i u sériového čísla, které se liší od původně prodaného sériového čísla.

Chcete-li konfigurovat ověření sériového čísla pro organizaci po zapnutí funkce **Sjednocené prostředí pro zpracování vrácení v POS**, přejděte v centrále Commerce na nabídku **Retail a Commerce \> Nastavení centrály \> Parametry \> Parametry obchodu**. Na kartě **Zásoby** nastavte na záložce s náhledem **Operace skladových zásob** možnost **Povolit ověřování sériových čísel u vrácení POS** na **Ano**.

## <a name="process-returns-for-serialized-items-in-pos"></a>Zpracování vratek u serializovaných položek v POS

Když je možnost **Povolit ověřování sériových čísel u vrácení POS** nastavena na **Ano** a položka řízená sériovým číslem je vrácena přes POS, může uživatel zadat sériové číslo pro řádek vratky v podokně podrobností na stránce **Vratné produkty**. Pokud je zadané sériové číslo jiné než původní sériové číslo, které bylo prodáno v prodejní transakci, obdrží uživatel varovnou zprávu. Aplikace však nebrání uživateli pokračovat v odeslání vratky.

> [!NOTE]
> V současné době POS podporuje ověřování sériových čísel pouze u řádků vrácení, kde původní objednané množství není větší než jedna. Pokud byl řádek původní prodejní objednávky vytvořen v kanálu nepatřícím do POS, a pokud je množství objednané pro serializovanou položku u daného řádku prodeje větší než jedna, nelze položku správně vrátit prostřednictvím POS.

## <a name="additional-resources"></a>Další prostředky

[Vytvoření vrácení v POS](POS-returns.md)
