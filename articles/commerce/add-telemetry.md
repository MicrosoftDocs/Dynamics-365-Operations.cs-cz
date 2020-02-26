---
title: Přidání kódu skriptu na webové stránky pro podporu telemetrie
description: V tomto tématu je popsán postup přidání kódu skriptu na straně klienta na stránky webu za účelem podpory kolekce telemetrie na straně klienta.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 674d00faf1b30f87a0b0062129e1b9fbff955dd4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001270"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Přidání kódu skriptu na webové stránky pro podporu telemetrie


[!include [banner](includes/banner.md)]

V tomto tématu je popsán postup přidání kódu skriptu na straně klienta na stránky webu za účelem podpory kolekce telemetrie na straně klienta.

## <a name="overview"></a>Přehled

Služba Web Analytics je základní nástroj, který umožňuje pochopit, jakým způsobem zákazníci komunikují s webem, a učinit rozhodnutí, která pomohou optimalizovat prostředí s maximálním vylazením. K dispozici je mnoho balíčků služby Web Analytics, které vám pomohou dosáhnout těchto cílů, jako jsou služby Google Analytics, Clicky, Moz Analytics a KISSMetrics. Většina balíčků služby Web Analytics vyžaduje přidání kódu skriptu na straně klienta do prvku **\<head\>** kódu HTML pro všechny stránky vašeho webu.

> [!NOTE]
> Pokyny v tomto tématu se vztahují také na jiné vlastní funkce na straně klienta, které řešení Microsoft Dynamics 365 Commerce nativně nenabízí.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Vytvoření opakovaně použitelného fragmentu kódu skriptu

Po vytvoření fragmentu kódu skriptu jej lze opakovaně použít na všech stránkách vašeho webu.

1. Přejde na **Fragmenty \> Nový fragment stránky**.
2. Vyberte možnost **Externískript**, zadejte název fragmentu a poté klikněte na tlačítko **OK**.
3. V hierarchii fragmentů vyberte pro fragment, který jste právě vytvořili, podřízený modul **Injektor skriptu**.
4. V podokně vlastností vpravo přidejte skript na straně klienta a nastavte další možnosti konfigurace podle potřeby.

## <a name="add-the-fragment-to-templates"></a>Přidání fragmentu do šablon

1. Přejděte na **Šablony** a otevřete šablonu pro stránky, na které chcete přidat kód skriptu.
2. V levém podokně rozbalte hierarchii šablon, aby se zobrazila pozice **Hlavička HTML**.
3. Vyberte tlačítko se třemi tečkami (**...**) vedle pozice **Hlavička HTML** a poté vyberte možnost **Přidat fragment**.
4. Vyberte fragment, který jste pro kód skriptu vytvořili.
5. Uložte šablonu a vraťte ji se změnami.

> [!NOTE]
> Po dokončení je nutné publikovat fragment a hlavní šablonu. 

## <a name="additional-resources"></a>Další zdroje

[Přidání loga](add-logo.md)

[Volba motivu webu](select-site-theme.md)

[Práce se soubory přepisu šablon CSS](css-override-files.md)

[Přidání ikony oblíbené položky](add-favicon.md)

[Přidání uvítací zprávy](add-welcome-message.md)

[Přidání oznámení o vlastnických právech](add-copyright-notice.md)

[Přidání jazyků na web](add-languages-to-site.md)

