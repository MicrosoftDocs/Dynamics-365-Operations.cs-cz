---
title: Práce se soubory přepisu CSS
description: Toto téma vysvětluje proč, kdy a jak používat soubory přepisu šablon Cascading Style Sheets (CSS) v produktu Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6788481936a54bff32096dba1d0424fc52c669e4
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/12/2022
ms.locfileid: "7964597"
---
# <a name="work-with-css-override-files"></a>Práce s CSS soubory přepisující výchozí styl

[!include [banner](includes/banner.md)]

Toto téma vysvětluje proč, kdy a jak používat soubory přepisu šablon Cascading Style Sheets (CSS) v produktu Microsoft Dynamics 365 Commerce.

Trvalé styly webu by obvykle měly být zpracovávány prostřednictvím motivu webu. Motivy poskytují základní nastavení šablon CSS a stylu pro moduly na libovolné stránce webu. Motivy jsou vytvářeny pomocí sady SDK Dynamics 365 Commerce (Software Development Kit) online a jsou nasazeny na vaše weby prostřednictvím aplikace Microsoft Dynamics Lifecycle Services (LCS). Možnosti ladění motivu a konfigurace rozhraní modulu v sadě SDK usnadňují vývojářům webu vytváření upravitelných a kohezivních balíčků návrhu webu. Pokud jsou tyto balíčky návrhu nasazeny na web, mohou se autoři webu zaměřit na vytváření, úpravy a publikování obsahu namísto vývoje webu.

Vzhledem k obvyklému životním cyklu motivu může být závislost na tom, aby vývojáři prováděli změny stylu prostřednictvím kanálu nasazení SDK a LCS, v některých scénářích příliš vysoká. Prototypy nebo opravy hotfix webů se mohou zdát těžko ovladatelné, pokud není konfigurovaná sada SDK nebo pokud nemáte čas čekat na nasazení LCS.

V těchto scénářích mohou pomoci soubory přepisu CSS. V nástrojích pro vytváření obchodních dat mohou ověření uživatelé odeslat soubor CSS, zobrazit jeho náhled a potom jej aktivovat, aby přepsal motiv webu. Nejsou nutné režijní náklady nasazení SDK nebo LCS. Přepisy, které jsou zadány v souboru přepisu CSS mohou být stejně malé jako změna jednoho stylu textu nebo rozsáhlé jako úplná revize značky.

Před použitím souborů přepisu CSS je třeba mít na zřeteli následující omezení:

- Na webu může být aktivní vždy pouze jeden soubor přepisu CSS. Proto musí být všechny aktivní přepisy přítomny v jediném souboru přepisu.
- Přestože můžete zobrazit náhled přepisů v nástrojích pro vytváření Commerce, nejsou k dispozici žádné vyhrazené funkce ladění, které by pomohly identifikovat chyby, jsou zavedeny při přepisech. Jinými slovy, pokud použijete soubory přepisu CSS, nemáte stejnou sadu nástrojů, kterou sada SDK poskytuje pro modul a pro ověření obsahu.

Soubory přepisu CSS však poskytují rychlý způsob navržení prototypu designu nebo implementace opravy hotfix před vyvinutím a nasazením aktualizace celého motivu.

## <a name="create-a-css-override-file"></a>Vytvoření souboru přepisu CSS

Chcete-li vytvořit soubor přepisu CSS, můžete použít jakékoli integrované vývojové prostředí (IDE), textový editor nebo editor zdrojového kódu. Typickým přístupem je použití standardních webových souborů ladění v prohlížeči k identifikaci selektorů, vlastností a hodnot stylu na existujícím webu. Většina prohlížečů umožňuje měnit hodnoty a zobrazovat jejich náhled v nástroji ladění. Po identifikaci změn, které chcete provést, můžete tyto změny uložit do vlastního souboru CSS.

## <a name="upload-a-css-override-file"></a>Odeslání souboru přepisu CSS

Pokud chcete odeslat soubor CSS na svůj web v Commerce, postupujte následovně.

1. Ve nástrojích pro tvorbu obsahu přejděte na svůj web.
1. V navigačním podokně nalevo vyberte položku **Návrh**.

    > [!NOTE]
    > V závislosti na verzi nástrojů pro vytváření obchodních dokumentů, kterou používáte, bude pravděpodobně nutné rozbalit **Nastavení** v navigačním podokně, aby bylo možné vybrat **Návrh**.

1. V horní části hlavního podokna návrhu vyberte kartu **Přepis CSS**, pokud již není vybraná.
1. V části **Dostupné přepisy CSS** vyberte **Nahrát soubor CSS**. Zobrazí se okno průzkumníka souborů.
1. V Průzkumníku souborů vyhledejte a vyberte soubor CSS a pak vyberte **otevřít**. Nahraný soubor CSS se nyní zobrazí v části **Dostupné přepisy CSS**.

## <a name="preview-a-css-override-file"></a>Náhled souboru přepisu CSS

Chcete-li zobrazit náhled CSS před tím, než soubor na aktivním webu aktivujete, postupujte takto:

1. V navigačním podokně vlevo vyberte **Návrh** a na kartě **Přepis CSS** v části **Dostupné přepisy CSS** vyhledejte soubor CSS, jehož náhled chcete zobrazit.
1. Vedle názvu souboru CSS vyberte **Web náhledu**.
1. V dialogovém okně **Vybrat adresu URL** vyberte adresu URL webu, na němž chcete zobrazit použitý přepis, a pak vyberte **OK**.
1. Pokud pro vybranou adresu URL existuje více variant, vyberte požadovanou variantu v dialogovém okně **Varianty návrhu**, které se zobrazí.

Otevře se nová karta nebo okno prohlížeče, kde můžete ověřit přepisy stylu vůči webu. Potom můžete tuto adresu URL sdílet s jinými ověřenými uživateli Commerce pro kontrolu a zpětnou vazbu.

## <a name="activate-a-css-override-file-on-your-live-site"></a>Aktivace souboru přepisu CSS na živém webu

Poté, co jste zobrazili náhled souboru přepisu CSS a schválili ho, můžete ho aktivovat na živém webu.

> [!NOTE]
> Na webu může být aktivní vždy pouze jeden soubor přepisu CSS. Pokud aktivujete nový soubor přepisu, předchozí soubor přepisu je deaktivován. Proto se ujistěte, že jsou všechny požadované přepisy přítomny v jednom souboru přepisu CSS.

Pokud chcete aktivovat soubor přepisu CSS, postupujte následujícím způsobem:

1. V navigačním podokně vlevo vyberte **Návrh** a na kartě **Přepis CSS** v části **Dostupné přepisy CSS** vyhledejte soubor CSS, jehož náhled chcete aktivovat.
1. Pod názvem souboru CSS vyberte **Aktivovat**. Soubor přepisu se okamžitě na vašem webu okamžitě aktivuje.

## <a name="deactivate-a-css-override-file-on-your-live-site"></a>Deaktivace souboru přepisu CSS na živém webu

Chcete-li deaktivovat soubor přepisu CSS na vašem webu, postupujte následovně.

1. V navigačním podokně vlevo vyberte **Návrh** a na kartě **Přepis CSS** v části **Dostupné přepisy CSS** vyhledejte soubor CSS, jehož náhled chcete deaktivovat.
1. Pod názvem souboru CSS vyberte **Deaktivovat**. Soubor přepisu se okamžitě na vašem webu okamžitě deaktivuje.

> [!TIP]
> Chcete-li získat přístup k dalším možnostem souborů přepisu CSS, vyberte tři tečky (**...**) vedle názvu souboru CSS. Možnosti **Stáhnout**, **Přejmenovat** a **Nahradit** jsou užitečné pro rychlé změny stávajícího souboru přepisu CSS.

## <a name="additional-resources"></a>Další prostředky

[Přidání loga](add-logo.md)

[Volba motivu webu](select-site-theme.md)

[Práce s předvolbami stylu](style-presets.md)

[Přidání ikony oblíbené položky](add-favicon.md)

[Přidání oznámení o vlastnických právech](add-copyright-notice.md)

[Přidání jazyků na web](add-languages-to-site.md)

[Přidání kódu skriptu na webové stránky pro podporu telemetrie](add-telemetry.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
