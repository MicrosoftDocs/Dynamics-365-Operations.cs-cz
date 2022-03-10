---
title: Přidání stránky se zásadami ochrany osobních údajů
description: Toto téma popisuje, jak přidat stránku se zásadami ochrany osobních údajů na web v řešení Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: faf2072a5c53aa84f0de2e6d2478557bf96b7832e3433ad4cba971bc3f6e5880
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729164"
---
# <a name="add-a-privacy-policy-page"></a>Přidání stránky se zásadami ochrany osobních údajů

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak přidat stránku se zásadami ochrany osobních údajů na web v řešení Microsoft Dynamics 365 Commerce.

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

1. Přejděte na **Šablony** a poté volbou **Nová** vytvořte šablonu stránky.
1. V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona propagačního banneru** a poté klikněte na tlačítko **OK**.
1. V šabloně přidejte všechny požadované moduly do požadovaných úseků stránky. Pokud chcete získat pokyny, najeďte ukazatelem myši na červené vykřičníky. (Úsek **Záhlaví HTML** může například vyžadovat modul **Výchozí externí skript**.)
1. Do úseku **Tělo** přidejte modul **Výchozí stránka**.
1. V modulu **Výchozí stránka** v úseku **Hlavní** přidejte modul **Blok s formátovaným obsahem**.
1. Do modulu **Blok s formátovaným obsahem** přidejte modul **Položka bloku s formátovaným obsahem**.
1. Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

### <a name="build-a-privacy-policy-page"></a>Sestavení stránky se zásadami ochrany osobních údajů

Chcete-li vytvořit stránku se zásadami ochrany osobních údajů, postupujte následovně.

1. Přejděte na **Stránky** a pak volbou **Nová** vytvořte stránku.
1. V dialogovém okně **Zvolte šablonu** vyberte šablonu pro stránku zásad ochrany osobních údajů.
1. Zadejte název a adresu URL stránky a poté klikněte na tlačítko **OK**. 
1. V pozici **Hlavní** na nové stránce přidejte modul **Blok s formátovaným obsahem**.
1. Do modulu **Blok s formátovaným obsahem** přidejte modul **Položka bloku s formátovaným obsahem**.
1. V podokně vlastností modulu **Blok s formátovaným obsahem** vyberte **Přidat zdroj dat** a pak vyberte **obsah ve formátu RTF**.
1. V editoru formátovaného textu zadejte obsah stránky zásad ochrany osobních údajů. Podle potřeby rozbalte Editor RTF do režimu celé obrazovky.
1. Po dokončení zadávání obsahu vyberte **náhled** k zobrazení náhledu stránky ve webovém prohlížeči.
1. Dokončete všechny zbývající dodatky k vlastnostem stránky a modulů.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

Chcete-li publikovat adresu URL pro stránku zásad ochrany osobních údajů, postupujte následovně.

1. Přejděte na **Adresy URL** a vyberte adresu URL stránky zásady ochrany osobních údajů.
1. Volbou **Publikovat** publikujte vybranou adresu URL.

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a>Vytvoření odkazu na stránku zásad ochrany osobních údajů v zápatí

Do fragmentu můžete přidat odkaz na stránku zásad ochrany osobních údajů. Tímto způsobem můžete odkaz sdílet a aktualizovat na více stránkách webu pomocí odkazu na fragment. Tento příklad ukazuje, jak přidat odkaz na stránku zásad ochrany osobních údajů do fragmentu zápatí.

Chcete-li přidat odkaz na fragment zápatí, postupujte takto.

1. Přejděte na **Fragmenty** a pak volbou **Nový** vytvořte fragment stránky.
1. V dialogovém okně **Nový fragment** vyberte modul **Zápatí**.
1. V části **Název fragmentu** zadejte název fragmentu a poté vyberte **OK**.
1. Do úseku **Kategorie zápatí** přidejte modul **Položka zápatí**.
1. V podokně vlastností vpravo vyberte možnost **Text odkazu**.
1. V dialogovém okně **Text odkazu** zadejte text odkazu a cíl odkazu na stránce Zásady ochrany osobních údajů a klikněte na tlačítko **OK.**
1. Chcete-li získat adresu URL stránky zásad ochrany osobních údajů, přejděte na **Stránky**, přejděte na stránku zásady ochrany osobních údajů a zkopírujte adresu URL z podokna vlastností.
1. Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.
1. Zobrazte náhled fragmentu a otestujte odkaz na stránku zásad ochrany osobních údajů.

Na fragment lze nyní odkazovat v šabloně pro jiné stránky webu. Pokud je na tento fragment odkazováno v modulu **Zápatí** šablony, reference odkazu se zobrazí na všech stránkách, které jsou vytvořeny pomocí této šablony.

## <a name="additional-resources"></a>Další zdroje

[Přehled dodržování předpisů](compliance-overview.md)

[Funkce a možnosti usnadnění přístupu](accessibility.md)

[Zásady zacházení se soubory cookie](cookie-compliance.md)

[Nahrazení ID uživatelů přidružených ke změnám sledovaných obsahů](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
