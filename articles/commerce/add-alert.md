---
title: Modul propagačního banneru
description: Tento článek se zabývá moduly propagačního banneru a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.openlocfilehash: fbde146923d1448e382cbf2458880f7e300f605c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279728"
---
# <a name="promo-banner-module"></a>Modul propagačního banneru

[!include [banner](includes/banner.md)]

Tento článek se zabývá moduly propagačního banneru a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.

Moduly propagačního banneru slouží k zobrazení vložených informačních zpráv na stránce. Lze je použít k zobrazení promoakcí v rámci celého webu, které se zobrazí na všech stránkách webu elektronického obchodu. 

Moduly propagačního banneru podporují textové zprávy a odkazy. Je-li do modulu propagačního banneru přidáno více zpráv, stane se bannerem rotujících karuselů, které umožňují zákazníkům cyklicky procházet všechny zprávy. 

Moduly propagačního banneru jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku.

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a>Příklady použití propagačního banneru v e-commerce

Reklamní bannery mohou být použity v záhlaví pracoviště pro zobrazení promoakcí a zpráv na úrovni celého pracoviště, jak je uvedeno v následujících příkladech.

„Výroční výprodej končí za 10 dnů“

„Ušetřete v předškolním výprodeji. Pusťte se do nakupování.“

„Využijte výproDEJ k Díkuvzdání!“ 

Na následujícím obrázku je znázorněn příklad propagačního banneru.

![Příklad modulu propagačního banneru.](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a>Vlastnosti modulu propagačního banneru

| Název vlastnosti             | Hodnota                              | popis |
|---------------------------|------------------------------------|-------------|
| Bannerové zprávy           | Text a odkazy                     | Pole textu a odkazů. |
| Přehrát automaticky                  | **Pravda** nebo **nepravda**              | Hodnota, která určuje, zda jsou zprávy automaticky cyklicky procházeny, pokud je konfigurováno více zpráv. |
| Interval přechodu snímků | Počet milisekund (MS)      | Interval, který se používá pro procházení zpráv. |
| Povolit zavření             | **Pravda** nebo **nepravda**              | Je-li tato hodnota nastavena na hodnotu **pravda**, zákazníci mohou výstrahu zavřít. |
| Zobrazit páku karuselu     | **Pravda** nebo **nepravda**              | Hodnota, která určuje, zda se mají zobrazit páky karuselu, aby zákazníci mohli ručně cyklovat více položek banneru. |
| Zarovnání textu            | **Vpravo**, **vlevo** nebo **uprostřed** | Zarovnání textu v modulu propagačního banneru. |
| Propojení                      | Adresa URL                              | Adresa URL pro volitelný odkaz. |
|Zarovnání textu             | **Vpravo**, **vlevo** nebo **uprostřed** | Tato vlastnost je k dispozici jako rozšíření motivu v motivu Adventure Works. Umožňuje uživateli nastavit zarovnání textu v propagačním banneru. |

> [!IMPORTANT]
> Motiv Adventure Works je k dispozici od Dynamics 365 Commerce verze 10.0.20.

## <a name="add-a-promo-banner-module-to-a-page"></a>Přidání modulu propagačního banneru na novou stránku 

Chcete-li přidat modul propagačního banneru na stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.

1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona propagačního banneru** a poté klikněte na tlačítko **OK**.
1. V části **Osnova stránky** přidejte modul **Výchozí stránka** do pozice **Hlavní část**. 
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte. 
1. Šablonu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka propagačního banneru**. 
1. V úseku **Hlavní** nové stránky přidejte modul kontejneru. 
1. V podokně napravo nastavte hodnotu **šířka** na **Vyplnit kontejner**.
1. V části **Osnova stránky** stránky přidejte do modulu kontejneru modul propgačního banneru.
1. V nastavení pro modul propgačního banneru přidejte jednu nebo více zpráv banneru. Každá zpráva může obsahovat text spolu s odkazem. Chcete-li dále upravit modul propgačního banneru, můžete upravit ostatní vlastnosti.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky. V horní části stránky by se měla zobrazit výstraha zobrazující text, který jste přidali.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

> [!NOTE]
> Propagační banner se obvykle používá v patici záhlaví stránky nebo v pozici dílčího hlavního záhlaví.

## <a name="additional-resources"></a>Další prostředky

[Přehled knihovny modulů](starter-kit-overview.md)

[Karuselový modul](add-carousel.md)

[Modul textového bloku](add-content-rich-block.md)

[Modul bloku obsahu](add-hero-module.md)

[Modul videopřehrávače](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
