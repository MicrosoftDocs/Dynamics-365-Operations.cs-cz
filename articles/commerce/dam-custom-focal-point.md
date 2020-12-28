---
title: Přizpůsobit fokální místa obrázku
description: Toto téma popisuje, jak přizpůsobit fokální místa obrázku v konfigurátoru webu Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
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
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b20fbc20f18243c712595795a0b16ae417e755e6
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594325"
---
# <a name="customize-image-focal-points"></a>Přizpůsobit fokální místa obrázku

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak přizpůsobit fokální místa obrázku v konfigurátoru webu Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Po odeslání obrazu do knihovny médií služby Commerce Services pro konfigurátor systému se systém pokusí určit fokální místo obrázku. Pokud například obrázek obsahuje osobu, systém ve výchozím nastavení nastaví fokální místo na obličej této osoby. Ve většině případů se automaticky nastaví fokální bod dobře pro všechna zobrazení, ale někdy můžete chtít upravit fokální bod, aby se zajistilo, že určitá část obrazu bude vždy viditelná.

### <a name="define-a-custom-focal-point-for-an-image"></a>Definovat vlastní fokální bod pro obrázek

Chcete-li definovat vlastní fokální bod pro obrázek, postupujte následujícím způsobem.

1. V levém navigačním podokně konfigurátoru webu Commerce vyberte položku **Knihovna médií**.
1. V hlavním okně vyberte obrázek, který chcete upravit.
1. Na příkazovém řádku vyberte možnost **Upravit**.
1. Vyberte obrázek pro **Režim úprav**.
1. V nabídce **Režim úprav** vyberte **Změnit fokální bod**. Nad obrázkem se zobrazí kruhový ovládací prvek fokálního bodu.
1. Vyberte ovládací prvek fokálního bodu, abyste jej přesunuli na požadovaný fokální bod.
1. Až skončíte, vyberte v panelu příkazů **Uložit** a pak vyberte **Dokončit úpravy**.

## <a name="additional-resources"></a>Další prostředky

[Přehled správy digitálních aktiv](dam-overview.md)

[Odeslání obrázků](dam-upload-images.md)

[Odeslání videa](dam-upload-video.md)

[Odeslat soubory](dam-upload-files.md)

[Oříznutí obrázků](dam-crop-images.md)

[Nahrání a obsloužení statických souborů](upload-serve-static-files.md)
