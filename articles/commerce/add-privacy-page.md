---
title: Přidání stránky se zásadami ochrany osobních údajů
description: Toto téma popisuje, jak přidat stránku se zásadami ochrany osobních údajů na web v řešení Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fd39ff5f8c5d97f2d524043b65627dc7e87fcf64
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945983"
---
# <a name="add-a-privacy-policy-page"></a>Přidání stránky se zásadami ochrany osobních údajů

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Toto téma popisuje, jak přidat stránku se zásadami ochrany osobních údajů na web v řešení Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Soulad s ochranou osobních údajů zahrnuje organizační opatření, která uživatele webu informují o způsobu sběru a zpracování jejich dat. Uživatelé se pak mohou rozhodnout, jak budou chtít zpracovat své osobní údaje, a mohou podniknout příslušné kroky.

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a>Projděte si prohlášení společnosti Microsoft o zásadách ochrany osobních údajů v Dynamics 365 Commerce

Pokud se chcete podívat na prohlášení o ochraně osobních údajů společnosti Microsoft, když jste přihlášení do vývojových nástrojů Dynamics 365 Commerce, klikněte na tlačítko **Nápověda** (**?**) v pravém horním rohu a pak vyberte **Zásady ochrany osobních údajů a soubory cookie**. Otevře se nová záložka, která obsahuje odkaz na [prohlášení o ochraně osobních údajů společnosti Microsoft](https://privacy.microsoft.com/privacystatement).

## <a name="build-a-privacy-policy-page-for-your-site"></a>Vytvoření stránky zásad ochrany osobních údajů pro váš web

V aplikaci Dynamics 365 Commerce existuje několik způsobů, jak poskytnout uživatelům přístup k vašim zásadám ochrany osobních údajů. V této části je uveden postup vytvoření stránky zásad ochrany osobních údajů a následné odkazování na stránku pomocí fragmentu zápatí.

Následující pokyny ukazují, jak vytvořit obecnou stránku zásad ochrany osobních údajů pro web Commerce. Jste zodpovědní za navržení a implementaci řešení stránky zásad ochrany osobních údajů, které nejlépe odpovídá právním požadavkům vaší společnosti.

Chcete-li začít, přejděte ve vývojových nástrojích na web, pro který chcete vytvořit stránku zásad ochrany osobních údajů.

### <a name="create-a-template"></a>Vytvořit šablonu

> [!NOTE]
> Pokud šablona, kterou lze použít pro stránku zásad ochrany osobních údajů, již byla vytvořena, přeskočte na část [Vytvoření stránky zásad ochrany osobních údajů](#build-a-privacy-policy-page).

Při vytváření šablony postupujte takto.

1. Přejděte na **Šablony \> Nová šablona**.
1. Zadejte název šablony a poté klikněte na tlačítko **OK**.
1. V šabloně přidejte všechny požadované moduly do požadovaných úseků stránky. Pokud chcete získat pokyny, najeďte ukazatelem myši na červené vykřičníky.

    Úsek **Záhlaví HTML** může například vyžadovat modul **Výchozí externí skript**.

1. Do úseku **Tělo** přidejte modul **Výchozí stránka**.
1. V modulu **Výchozí stránka** v úseku **Hlavní** přidejte modul **Blok s formátovaným obsahem**.
1. Do modulu **Blok s formátovaným obsahem** přidejte modul **Položka bloku s formátovaným obsahem**.
1. Vraťte šablonu se změnami a publikujte ji.

### <a name="build-a-privacy-policy-page"></a>Sestavení stránky se zásadami ochrany osobních údajů

Chcete-li vytvořit stránku se zásadami ochrany osobních údajů, postupujte následovně.

1. Přejděte na **Stránky \> Nová stránka**.
1. Vyberte šablonu pro stránku zásad ochrany osobních údajů.
1. Zadejte název a adresu URL šablony a poté klikněte na tlačítko **OK**. 
1. V pozici **Hlavní** na nové stránce přidejte modul **Blok s formátovaným obsahem**.
1. Do modulu **Blok s formátovaným obsahem** přidejte modul **Položka bloku s formátovaným obsahem**.
1. V podokně vlastností modulu **Blok s formátovaným obsahem** vyberte **Přidat zdroj dat** a pak vyberte **obsah ve formátu RTF**.
1. V editoru formátovaného textu zadejte obsah stránky zásad ochrany osobních údajů. Podle potřeby rozbalte Editor RTF do režimu celé obrazovky.
1. Po dokončení zadávání obsahu vyberte **náhled** k zobrazení náhledu stránky ve webovém prohlížeči.
1. Dokončete všechny zbývající dodatky k vlastnostem stránky a modulů.
1. Vraťte stránku se zásadami ochrany osobních údajů a publikujte ji.

Chcete-li publikovat adresu URL pro stránku zásad ochrany osobních údajů, postupujte následovně.

1. Přejděte na **Adresy URL** a vyberte adresu URL stránky zásady ochrany osobních údajů.
1. Publikujte vybranou adresu URL.

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>Vytvoření odkazu na stránku zásad ochrany osobních údajů v zápatí

Do fragmentu můžete přidat odkaz na stránku zásad ochrany osobních údajů. Tímto způsobem můžete odkaz sdílet a aktualizovat na více stránkách webu pomocí odkazu na fragment. Tento příklad ukazuje, jak přidat odkaz na stránku zásad ochrany osobních údajů do fragmentu zápatí.

Chcete-li přidat odkaz na fragment zápatí, postupujte takto.

1. Přejděte na **Fragmenty stránky \> Nový fragment stránky**.
1. Vyberte modul **zápatí** a pak zadejte název do pole **Název fragmentu stránky**.
1. Do úseku **Kategorie zápatí** přidejte modul **Položka zápatí**.
1. V podokně vlastností vpravo vyberte možnost **Text odkazu**.
1. V dialogovém okně **Text odkazu** zadejte text odkazu a cíl odkazu na stránce Zásady ochrany osobních údajů a klikněte na tlačítko **OK.**

    Chcete-li získat adresu URL stránky zásad ochrany osobních údajů, přejděte na **Stránky**, přejděte na stránku zásady ochrany osobních údajů a zkopírujte adresu URL z podokna vlastností.

1. Uložte fragment stránky, vraťte jej se změnami a publikujte.
1. Zobrazte náhled fragmentu a otestujte odkaz na stránku zásad ochrany osobních údajů.

Na fragment lze nyní odkazovat v šabloně pro jiné stránky webu. Pokud je na tento fragment odkazováno v modulu **Zápatí** šablony, reference odkazu se zobrazí na všech stránkách, které jsou vytvořeny pomocí této šablony.

## <a name="additional-resources"></a>Další zdroje

[Přehled dodržování předpisů](compliance-overview.md)

[Funkce a možnosti usnadnění přístupu](accessibility.md)

[Zásady zacházení se soubory cookie](cookie-compliance.md)
