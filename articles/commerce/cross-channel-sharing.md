---
title: Povolení a používání sdílení napříč kanály
description: Toto téma popisuje, jak povolit a používat funkci sdílení napříč kanály v konfigurátoru webů Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: de317c2fae4607f5b8b887dd5e866d812043dcd3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799510"
---
# <a name="enable-and-use-cross-channel-sharing"></a>Povolení a použití sdílení napříč kanály

[!include [banner](includes/banner.md)]

Toto téma popisuje, jak povolit a používat funkci sdílení napříč kanály v konfigurátoru webů Microsoft Dynamics 365 Commerce.

Sdílení napříč kanály umožňuje maloobchodníkům opakovaně používat a sdílet obsah mezi několika kanály webu. Tuto schopnost oceníte, pokud mají kanály webu kompatibilní základní jazyk nebo pokud mají mnoho společných položek obsahu.

Sdílení napříč kanály funguje tak, že se povolí výchozí kanál, ve kterém se bude hledat dostupný obsah, pokud se nenajde verze požadovaného obsahu pro konkrétní kanál. Obsah, který má být sdílen mezi kanály, se vytváří ve výchozím kanálu. Tento obsah lze lokalizovat do libovolného národního prostředí, které se u kanálu webu používá.

## <a name="when-to-use-cross-channel-sharing"></a>Když použít sdílení napříč kanály

Sdílení napříč kanály je užitečné, když několik kanálů na jednom webu sdílí obsah. Například maloobchodník, který má několik značek a poutačů seskupených na jednom webu, může sdílet určitý obsah mezi některými nebo všemi poutači. Tímto sdíleným obsahem mohou být stránky s podmínkami a ujednáními, platebními podmínkami, způsoby dopravy a často kladenými dotazy.

Sdílení napříč kanály také podporuje fragmenty. Stránku obsahu, na které jsou fragmenty specifické pro kanál, lze proto vytvořit jako obsah pro více kanálů. Ačkoli bude většina obsahu sdílena mezi kanály, budou fragmenty specifické pro kanál na stránce pro více kanálů vykresleny jen v případě, že jsou vyžádány z příslušného kanálu poutače.

Weby, které mají jen jeden kanál, nebo weby, které mají několik kanálů bez sdílení obsahu, nebudou sdílení napříč kanály využívat.

## <a name="enable-cross-channel-sharing"></a>Povolení sdílení napříč kanály

Sdílení napříč kanály se povoluje na úrovni webu. Tato operace je jednosměrná. Jinými slovy, pokud sdílení napříč kanály povolíte, nedá se zakázat.

Sdílení napříč kanály povolíte v konfigurátoru webů Commerce tímto postupem.

1. Přejděte na **Nastavení webu \> Funkce**.
1. Možnost **Napříč kanály** nastavte na **Zapnuto**.

    ![Možnost Napříč kanály nastavená na Zapnuto v konfigurátoru webů Commerce](./media/enabling-cross-channel-sharing.png)

Po povolení sdílení napříč kanály se informace pro více kanálů objeví v sekci **Kanály** v oblasti **Nastavení webu \> Funkce**, jak ukazuje příklad na následujícím obrázku.

![Informace kanálů viditelné po povolení sdílení napříč kanály](./media/channels-cross-channel.png)

Jakmile povolíte sdílení napříč kanály, bude pole **Kanál** v pravém horním rohu konfigurátoru webů Commerce obsahovat možnost **Online obchod s více kanály**, kterou můžete použít ke správě obsahu pro více kanálů, jak znázorňuje následující obrázek.

![Možnost Online obchod s více kanály v poli Kanály po povolení sdílení napříč kanály](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a>Vytvoření a používání obsahu pro více kanálů

Obsah pro více kanálů můžete vytvářet a používat několika způsoby. Můžete například vytvořit fragmenty pro více kanálů, vytvořit stránky pro více kanálů, které používají obsah pro více kanálů a obsah specifický pro kanál, a přepsat fragmenty pro více kanálů pomocí verzí fragmentů specifických pro kanál.

### <a name="create-a-cross-channel-fragment"></a>Vytvoření fragmentu pro více kanálů

Fragment pro více kanálů vytvoříte v konfigurátoru webů Commerce tímto postupem.

1. Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.
1. V dialogovém okně **Nový fragment** vyberte modul **Propagační banner** a pak v oblasti **Název fragmentu** zadejte název (například **Banner pro více kanálů**). Pak vyberte **OK**.
1. V podokně vlastností modulu **Propagační banner** vyberte **Přidat zprávu** a potom vyberte **Zpráva**.
1. V dialogovém okně **Zpráva** v oblasti **Text** zadejte **Pro více kanálů** a pak vyberte **OK**. 
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

Tento fragment pro více kanálů lze použít na stránkách pro více kanálů nebo specifických pro kanál, které jsou vytvořeny na libovolném kanálu webu.

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a>Vytvoření stránky pro více kanálů, která používá obsah pro více kanálů

Stránky pro více kanálů lze použít v jakémkoli kanálu vašeho webu. Stránku sdíleného obsahu proto stačí vytvořit jednou a následně provádět všechny aktualizace na jednom místě. Například stránku pro více kanálů **Podmínky a ujednání**, jejíž adresa URL je `/toc`, lze sdílet mezi všemi kanály webu. Pokud jsou základní adresy URL kanálů webu `www.fabrikam.com/brand1` a `www.fabrikam.com/brand2`, bude stejná sdílená stránka pro více kanálů **Podmínky a ujednání** dostupná z obou adres URL kanálu webu, a sice `www.fabrikam.com/brand1/toc` a `www.fabrikam.com/brand2/toc`. Pokud musí být stránka **Podmínky a ujednání** později aktualizována, stačí aktualizovat jen jednu sdílenou stránku.

Pokud chcete v konfigurátoru webů Commerce vytvořit stránku pro více kanálů, která používá obsah pro více kanálů, použijte následující postup.

1. Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.
1. V dialogovém okně **Zvolte šablonu** vyberte některou šablonu, například **Marketing**.
1. V poli **Název stránky** zadejte název stránky (například **Stránka pro více kanálů**).
1. V poli **Adresa URL stránky** zadejte adresu URL stránky (například **examplepage**) a pak vyberte **OK**.
1. V pozici **Hlavní** na nové stránce vyberte tři tečky (**...**) a vyberte možnost **Přidat fragment**.
1. V dialogovém okně **Přidat fragment** vyberte fragment pro více kanálů s propagačním bannerem, který jste vytvořili dříve, a vyberte **OK**.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky. Měli byste vidět propagační banner s textem „Pro více kanálů“.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a>Vytvoření stránky specifické pro kanál, která používá obsah pro více kanálů

Při použití obsahu pro více kanálů na stránkách specifických pro kanál můžete jednou vytvořit sdílený fragment obsahu a pak ho použít na stránkách specifických pro kanál. Tento „jediný zdroj“ je užitečný pro sdílený obsah, jako jsou podmínky a ujednání, platební podmínky nebo kontaktní informace.

Pokud chcete v konfigurátoru webů Commerce vytvořit stránku specifickou pro kanál, která používá obsah pro více kanálů, použijte následující postup.

1. Z konkrétního kanálu, například **Rozšířený online obchod Fabrikam**, přejděte na **Stránky** a výběrem možnosti **Nový** vytvořte novou stránku.
1. V dialogovém okně **Zvolte šablonu** vyberte některou šablonu, například **Marketing**.
1. V poli **Název stránky** zadejte název stránky (například **Stránka specifická pro kanál**).
1. V poli **Adresa URL stránky** zadejte adresu URL stránky (například **channelspecificpage**) a pak vyberte **OK**.
1. V pozici **Hlavní** na nové stránce vyberte tři tečky (**...**) a vyberte možnost **Přidat fragment**.
1. V dialogovém okně **Přidat fragment** v oblasti **Kanál** vyberte **Online obchod s více kanály**. V seznamu by se měl objevit fragment pro více kanálů, který jste vytvořili dříve. Vyberte ho a pak vyberte **OK**.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky. Měli byste vidět propagační banner s textem „Pro více kanálů“.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a>Vytvoření verze stránky pro více kanálů specifické pro kanál

Sdílení napříč kanály podporuje přepsání obsahu pro více kanálů. Všechny kanály vašeho webu kromě jednoho například sdílejí stejný obsah. Tento jeden kanál webu vyžaduje odlišný obsah. Pokud pro něj chcete implementovat odlišný obsah, vytvořením verze stránky pro více kanálů specifické pro kanál přepíšete obsah pro více kanálů obsahem specifickým pro kanál.

Pokud chcete v konfigurátoru webů Commerce vytvořit verzi stránky pro více kanálů specifickou pro kanál, použijte následující postup.

1. V poli **Kanál** v pravém horním rohu vyberte **Online obchod s více kanály**.
1. Otevřete stránku pro více kanálů, kterou jste vytvořili dříve.
1. V poli **Kanál** v pravém horním rohu vyberte kanál, který má mít specifický obsah. Editor stránky zobrazí zprávu, která vás vyzve k vytvoření nové varianty stránky.
1. Vyberte **Vytvořit variantu stránky**.
1. V pozici **Hlavní** na variantě stránky vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.
1. V dialogovém okně **Přidat modul** vyberte modul **Propagační banner** a pak vyberte **OK**.
1. V podokně vlastností modulu **Propagační banner** vyberte **Přidat zprávu** a potom vyberte **Zpráva**.
1. V dialogovém okně **Zpráva** v oblasti **Text** zadejte **Specifické pro kanál** a vyberte **OK**.
1. Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky. Měli byste vidět propagační banner s textem „Specifické pro kanál“.
1. Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.

Když teď použijete základní adresu URL kanálu a přejdete na adresu URL stránky pro více kanálů na tomto webu, uvidíte místo obsahu pro více kanálů obsah specifický pro tento kanál.

## <a name="additional-resources"></a>Další prostředky

[Způsoby přidání obsahu](add-manage-content.md)

[Glosář modelu stránky](page-elements-overview.md)

[Stavy dokumentu a životního cyklu](document-states-overview.md)

[Práce s publikovacími skupinami](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
