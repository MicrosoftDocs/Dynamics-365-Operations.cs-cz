---
title: Přidání kódu skriptu na webové stránky pro podporu telemetrie
description: V tomto tématu je popsán postup přidání kódu skriptu na straně klienta na stránky webu za účelem podpory kolekce telemetrie na straně klienta.
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: a88f4f920154aafaa15a48af67365152e21111f7
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761242"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a>Přidání kódu skriptu na webové stránky pro podporu telemetrie

[!include [banner](includes/banner.md)]

V tomto tématu je popsán postup přidání kódu skriptu na straně klienta na stránky webu za účelem podpory kolekce telemetrie na straně klienta.

## <a name="overview"></a>Přehled

Služba Web Analytics je základní nástroj, který umožňuje pochopit, jakým způsobem zákazníci komunikují s webem, a učinit rozhodnutí, která pomohou optimalizovat prostředí s maximálním vylazením. K dispozici je mnoho balíčků služby Web Analytics, které vám pomohou dosáhnout těchto cílů, jako jsou služby Google Analytics, Clicky, Moz Analytics a KISSMetrics. Většina balíčků služby Web Analytics vyžaduje přidání kódu skriptu na straně klienta do prvku **\<head\>** kódu HTML pro všechny stránky vašeho webu.

> [!NOTE]
> Pokyny v tomto tématu se vztahují také na jiné vlastní funkce na straně klienta, které řešení Microsoft Dynamics 365 Commerce nativně nenabízí.

## <a name="create-a-reusable-fragment-for-your-script-code"></a>Vytvoření opakovaně použitelného fragmentu kódu skriptu

Fragment umožňuje opakované použití vloženého nebo vnějšího kódu skriptu na všech stránkách vašeho webu bez ohledu na použitou šablonu.

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a>Vytvoření opakovaně použitelného fragmentu pro váš kód vloženého skriptu

Chcete-li vytvořit opakovaně použitelný fragment pro vložený kód skriptu v rámci konfigurátoru webu, postupujte podle následujících kroků.

1. Přejděte na **Fragmenty** a pak vyberte **Nový**.
1. V dialogovém okně **Nový fragment** vyberte **Vložený skript**.
1. V části **Název fragmentu** zadejte název fragmentu a poté vyberte **OK**.
1. V rámci vytvořeného fragmentu vyberte modul **Výchozí vložený skript**.
1. V podokně vlastností vpravo v části **vložený skript**zadejte skript na straně klienta. Poté nakonfigurujte další možnosti podle potřeby.
1. Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.
1. Zvolte **Publikovat**.

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a>Vytvoření opakovaně použitelného fragmentu pro váš kód externího skriptu

Chcete-li vytvořit opakovaně použitelný fragment pro externí kód skriptu v rámci konfigurátoru webu, postupujte podle následujících kroků.

1. Přejděte na **Fragmenty** a pak vyberte **Nový**.
1. V dialogovém okně **Nový fragment** vyberte **Externí skript**.
1. V části **Název fragmentu** zadejte název fragmentu a poté vyberte **OK**.
1. V rámci vytvořeného fragmentu vyberte modul **Výchozí externí skript**.
1. V podokně vlastností vpravo v části **Zdroj skriptu** přidejte externí nebo relativní adresu URL pro externí zdroj skriptu. Poté nakonfigurujte další možnosti podle potřeby.
1. Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.
1. Zvolte **Publikovat**.

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a>Přidání fragmentu, který zahrnuje kód skriptu, do šablony

Chcete-li přidat fragment, který obsahuje kód skriptu, do šablony v konfigurátoru webů, postupujte podle následujících kroků.

1. Přejděte na **Šablony** a otevřete šablonu pro stránky, na které chcete přidat kód skriptu.
1. V levém podokně rozbalte hierarchii šablon, aby se zobrazila pozice **Hlavička HTML**.
1. V pozici **Hlavička HTML** vyberte tlačítko se třemi tečkami (**...**) a poté vyberte možnost **Přidat fragment**.
1. Vyberte fragment, který jste pro kód skriptu vytvořili.
1. Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.
1. Zvolte **Publikovat**.

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a>Přidání externího skriptu nebo vloženého skriptu přímo do šablony

Chcete-li vložit vložený nebo externí skript přímo do sady stránek, která je řízena jedinou šablonou, nemusíte nejprve vytvořit fragment.

### <a name="add-an-inline-script-directly-to-a-template"></a>Přidání vloženého skriptu přímo do šablony

Chcete-li přidat vložený skript přímo do šablony v rámci konfigurátoru webu, postupujte podle následujících kroků.

1. Přejděte na **Šablony** a otevřete šablonu pro stránky, na které chcete přidat kód skriptu.
1. V levém podokně rozbalte hierarchii šablon, aby se zobrazila pozice **Hlavička HTML**.
1. V pozici **Hlavička HTML** vyberte tlačítko se třemi tečkami (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte **vložený skript**.
1. V podokně vlastností vpravo v části **vložený skript**zadejte skript na straně klienta. Poté nakonfigurujte další možnosti podle potřeby.
1. Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.
1. Zvolte **Publikovat**.

### <a name="add-an-external-script-directly-to-a-template"></a>Přidání externího skriptu přímo do šablony

Chcete-li přidat externí skript přímo do šablony v rámci konfigurátoru webu, postupujte podle následujících kroků.

1. Přejděte na **Šablony** a otevřete šablonu pro stránky, na které chcete přidat kód skriptu.
1. V levém podokně rozbalte hierarchii šablon, aby se zobrazila pozice **Hlavička HTML**.
1. V pozici **Hlavička HTML** vyberte tlačítko se třemi tečkami (**...**) a poté vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte **Externí skript**.
1. V podokně vlastností vpravo v části **Zdroj skriptu** přidejte externí nebo relativní adresu URL pro externí zdroj skriptu. Poté nakonfigurujte další možnosti podle potřeby.
1. Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.
1. Zvolte **Publikovat**.

## <a name="additional-resources"></a>Další prostředky

[Přidání loga](add-logo.md)

[Volba motivu webu](select-site-theme.md)

[Práce se soubory přepisu šablon CSS](css-override-files.md)

[Přidání ikony oblíbené položky](add-favicon.md)

[Přidání uvítací zprávy](add-welcome-message.md)

[Přidání oznámení o vlastnických právech](add-copyright-notice.md)

[Přidání jazyků na web](add-languages-to-site.md)
