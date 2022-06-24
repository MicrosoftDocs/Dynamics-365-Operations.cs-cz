---
title: Mapování kanálů na weby elektronického obchodování
description: Tento článek popisuje některé z běžnějších scénářů mapování kanálů v Microsoft Dynamics 365 Commerce, které lze extrapolovat pro většinu ostatních obchodních požadavků.
author: samjarawan
ms.date: 05/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 94c43df26e8d6e55a5b6d459b65066d5873e1063
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902756"
---
# <a name="map-channels-to-e-commerce-sites"></a>Mapování kanálů na weby elektronického obchodování

Tento článek popisuje některé z běžnějších scénářů mapování kanálů v Microsoft Dynamics 365 Commerce, které lze extrapolovat pro většinu ostatních obchodních požadavků.

Dynamics 365 Commerce podporuje mnoho obchodních scénářů pro mapování [online kanálů](#channels), které mají nakonfigurovanou sadu produktů, cen a slev [stránky elektronického obchodu](#e-commerce-sites) pro zákazníky.

Tento článek pokrývá následující scénáře:

- **Jednojazyčný kanál s jedním webem elektronického obchodu.** Tento scénář může například zahrnovat web jedné značky, který je nakonfigurován pro americký anglický trh.
- **Vícejazyčný kanál s jedním lokalizovaným webem elektronického obchodu.** Tento scénář může například zahrnovat web jedné značky, který je nakonfigurován pro Kanadu s podporou francouzštiny a angličtiny. V tomto scénáři mají uživatelé, kteří vyberou různé jazyky, stejné prostředí webu, ale je lokalizováno do jazyka zvoleného každým uživatelem.
- **Vícejazyčný kanál s více lokalizovanými weby elektronického obchodu.** Tento scénář může například zahrnovat web jedné značky, který je nakonfigurován pro Kanadu s podporou francouzštiny a angličtiny. V tomto scénáři existuje pro každý jazyk jedinečné prostředí webu.
- **Více kanálů (jednojazyčných a/nebo vícejazyčných), které mají jeden lokalizovaný web.** Tento scénář může například zahrnovat web jedné značky, který je nakonfigurován pro Austrálii a Nový Zéland. V tomto scénáři obě země sdílejí stejné prostředí webu v angličtině, ale každá země je nakonfigurována s jinými produkty, měnou, cenami, slevami a způsoby dopravy.
- **Více kanálů (jednojazyčných a/nebo vícejazyčných), které mají různé weby na kanál.** Tento scénář může například zahrnovat web jedné značky, který je nakonfigurován pro Austrálii, Kanadu a Německo ve více jazycích. V tomto scénáři všechny země mají jedinečné prostředí webu v angličtině, ale každá země je nakonfigurována s jinými produkty, měnou, cenami, slevami a způsoby dopravy.

## <a name="channels"></a>Kanály

Kanál (také známý jako online obchod nebo online kanál) představuje výlohu online elektronického obchodu, která se používá k mapování produktů, cen, slev, jazyků, platebních metod, způsobů doručení, distribučních center a dalších aspektů online prostředí, které budou k dispozici zákazníkům vašeho e-shopu. Kanály jsou vytvářeny a spravovány v centrále Commerce a jsou mapovány na jednu [právnickou osobu](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json#legal-entities). Právnická osoba má obvykle sídlo v jedné zemi, která u kanálu vyžaduje daňové vykazování, a lze u ní konfigurovat pouze jedinou měnu.

Další informace o kanálech naleznete v [Přehledu kanálů](channels-overview.md). Další informace o tom, jak vytvořit online kanál, najdete v článku [Nastavení online kanálu](channel-setup-online.md).

Následující ukázkový obrázek z centrály Commerce ukazuje výchozí online kanály, které jsou nasazeny v Dynamics 365 Commerce, pokud je vybrána možnost ukázkových dat.

![Výchozí ukázkové datové kanály v centrále Commerce.](media/channel-mapping-1.png)

## <a name="e-commerce-sites"></a>Weby elektronického obchodu

Web elektronického obchodu obsahuje sadu webových stránek, které zákazníci používají k procházení a nakupování. Weby elektronického obchodování jsou spravovány v nástroji Commerce Site Builder.

Další informace o vytváření a správě webů v nástroji Site Builder naleznete v článku [Přehled webu elektronického obchodu](online-store-overview.md).

## <a name="common-channel-mapping-scenarios"></a>Běžné scénáře mapování kanálů

Dynamics 365 Commerce podporuje širokou škálu scénářů mapování kanálů. Následující scénáře mapování kanálů jsou pouze podmnožinou všech možných scénářů mapování kanálů. Jsou určeny jako vodítko, které vám pomůže naplánovat jakékoli jedinečné obchodní scénáře, které máte. Fiktivní obchod se sportovním zbožím Adventure Works, který je součástí ukázkových dat Dynamics 365 Commerce, je použit v každém scénáři jako příklad.

### <a name="single-language-channel-that-has-a-single-e-commerce-site-experience"></a>Jednojazyčný kanál s jedním prostředím webu elektronického obchodu

V nejzákladnějším scénáři má jeden kanál jeden jazyk pro prodej na jednom trhu. Příkladem tohoto scénáře je online obchod Adventure Works, který má nastavenu pouze americkou angličtinu.

Následující ilustrace ukazuje příklad konfigurace kanálu v centrále Commerce. V této konfiguraci online kanál podporuje pouze jeden jazyk (**en-us**), jednu měnu (**americký dolar**) a jednu obchodní entitu (**usrt**), která se používá pro daňové vykazování.

![Právnická osoba, měna a jazykové hodnoty pro online obchod Adventure Works zvýrazněné v centrále Commerce.](media/channel-mapping-3.png)

Jediný online kanál lze v nástroji pro tvorbu webu namapovat na jeden web elektronického obchodu. Informace o tom, jak vytvořit nový web a namapovat jej na kanál, naleznete v sekci [Mapování kanálu na web v nástroji pro tvorbu webu](#map-a-channel-to-a-site-in-site-builder) tohoto článku.

### <a name="multi-language-channel-that-has-a-single-localized-site-experience"></a>Vícejazyčný kanál s jedním lokalizovaným webem elektronického obchodu

V tomto scénáři jeden kanál podporuje více než jeden jazyk. Proto lze názvy produktů, popisy a atributy v centrále Commerce lokalizovat. Chcete-li poskytnout kompletní lokalizované prostředí, marketingový obsah na webu lze lokalizovat také v nástroji Commerce Site Builder.

Omezení tohoto scénáře spočívá v tom, že u jednoho kanálu lze konfigurovat pouze jednu měnu, jednu právnickou osobu a jednu sadu produktů a cen. Tato konfigurace funguje nejlépe u zemí, které mají jednu měnu a kde se mluví více jazyky (například Kanada, kde se mluví anglicky a francouzsky), jednu právnickou osobu a jednu sadu produktů a cen.

Každý jazyk v kanálu může mít konfigurován vlastní název domény. Například doména `www.adventure-works.ca` bude určena pro kanadskou anglickou verzi a doména `www.adventure-works-fr.ca` pro kanadskou francouzskou verzi. Alternativně lze v jedné doméně konfigurovat různé jazyky v kanálu a pro každý jazyk použít jinou cestu. Například doména `www.adventure-works.ca` bude určena pro kanadskou anglickou verzi a cesta `www.adventure-works.ca/fr` bude použita pro kanadskou francouzskou verzi. Je také možné povolit [geografickou detekci](geo-detection-redirection.md) a použít ji k automatickému přesměrování uživatele na správný web na základě polohy uživatele.

Informace o tom, jak zákazníkům umožnit ruční přepínání mezi jazyky, naleznete v sekci [Přidání a konfigurace modulu pro výběr webu](#add-and-configure-the-site-picker-module) tohoto článku. Informace o tom, jak přizpůsobit lokalizované stránky a fragmenty, naleznete v sekci [Správa obsahu webu, který má více kanálů a jazyků](#manage-site-content-that-has-multiple-channels-and-languages).

### <a name="multi-language-channel-that-has-a-different-site-experience-per-language"></a>Vícejazyčný kanál s více lokalizovanými weby elektronického obchodu

Můžete dát přednost scénáři, kdy jeden kanál podporuje více než jeden jazyk, ale pro každý jazyk se vykresluje úplně jiný web. Doporučenou metodou pro implementaci tohoto scénáře je použít [varianty stránky](#implement-page-variants-for-each-language) na jediném webu.

Další metodou je vytvořit nový web elektronického obchodu pro každý jazyk v nástroji pro tvorbu webu a poté namapovat každý web na jeden online kanál a jazyk. Výsledkem bude jeden online kanál, který je namapován na několik webů elektronického obchodování, jeden pro každý jazyk. Tato metoda s více weby vyžaduje další prostředky pro správu, protože v nástroji pro tvorbu webů bude nutné spravovat více než jeden web.

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-single-localized-site-experience"></a>Více kanálů (jednojazyčných a/nebo vícejazyčných), které mají jeden lokalizovaný web

Značkový web může vyžadovat více online kanálů na jeden region, aby podporovaly jinou měnu, sadu produktů a sadu cen pro každý kanál na jednom webu. Například web Adventure Works může mít online kanál pro kanadský trh s více jazyky, kanál pro americký trh s jedním jazykem a kanál pro německý trh s jedním jazykem. V tomto scénáři bude mít každý online kanál konfigurovánu právnickou osobu specifickou pro daný region, a může mít stejnou sadu produktů jako jiné kanály, podmnožinu těchto produktů nebo jinou sadu produktů. Každý kanál bude mít také své vlastní ceny v regionální měně, daně, slevy a způsoby dopravy.

V tomto scénáři může mít každý trh nastaven vlastní názvy domén. Například doména `www.adventure-works.com` bude určena pro USA trh a doména `www.adventure-works.de` pro německý trh. Alternativně lze každý trh konfigurovat tak, aby používal jinou cestu. Například doména `www.adventure-works.com` bude určena pro USA trh a cesta `www.adventure-works.com/de` pro německý trh. Je také možné povolit [geografickou detekci](geo-detection-redirection.md) a použít ji k automatickému přesměrování uživatelů na správný web na základě regionu uživatele.

Můžete také chtít, aby web obsahoval rozevírací seznam, který uživatelům umožní ručně přepnout na konkrétní trh. Další informace naleznete v sekci [Přidání a konfigurace modulu pro výběr webu](#add-and-configure-the-site-picker-module) v tomto článku.

Informace o konfiguraci více kanálů na jednom webu naleznete v sekci [Konfigurace více kanálů na webu elektronického obchodu](#configure-multiple-channels-on-an-e-commerce-site).

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-different-site-experience-per-channel"></a>Více kanálů (jednojazyčných a/nebo vícejazyčných), které mají různé weby na kanál

Možná chcete mít více kanálů pro jednu značku v různých regionech a možná chcete, aby každý region měl jiné prostředí webu. Tento scénář lze implementovat dvěma způsoby:

- Použijte [varianty stránek](#implement-page-variants-for-each-language).
- V nástroji pro tvorbu webů nakonfigurujte pro každý online kanál jiný web a poté každý web namapujte na jiný online kanál a jazyk. Tato metoda vyžaduje další prostředky pro správu, protože v nástroji pro tvorbu webů bude nutné spravovat více než jeden web.

## <a name="cross-channel-sharing"></a>Sdílení napříč kanály

Sdílení napříč kanály je užitečné, když několik kanálů na jednom webu sdílí obsah. Například maloobchodník, který má několik značek a poutačů seskupených na jednom webu, může sdílet určitý obsah mezi některými nebo všemi poutači. Sdíleným obsahem mohou být stránky s podmínkami a ujednáními, platebními podmínkami, způsoby dopravy a často kladenými dotazy. Více informací najdete v tématu [Povolení a použití sdílení napříč kanály](cross-channel-sharing.md).

## <a name="map-a-channel-to-a-site-in-site-builder"></a>Mapování kanálu na web v nástroji pro tvorbu webu

Existuje několik způsobů vytváření a konfigurace webů, které mají používat více online kanálů.

### <a name="create-a-new-site"></a>Vytvoření nového webu

Zcela nový web můžete vytvořit v nástroji Site Builder tak, že přejdete na stránku **Weby** a vyberete možnost **Nový web**. Poté v dialogu **Nový web**, který se zobrazí, můžete vybrat výchozí online kanál a jazyk webu, jak je znázorněno na následujícím příkladu.

![Vytvoření nového kanálu v nástroji pro tvorbu webu.](media/channel-mapping-4.png)

Web, který vytvoříte tímto způsobem, bude prázdný a nebude obsahovat žádné stránky webu (například domovskou stránku, stránky kategorií a stránky produktů).

Další informace najdete v části [Vytvoření webu elektronického obchodu](create-ecommerce-site.md).

### <a name="create-a-new-site-by-using-the-site-copy-operation"></a>Vytvoření nového webu kopírováním jiného webu

Namísto vytvoření zcela nového prázdného webu, jak je popsáno v předchozí části, je lepší začít s kopií jednoho ze startovacích webů, které jsou k dispozici v knihovně modulů Commerce, jako je web Fabrikam nebo Adventure Works.

Chcete-li zkopírovat existující web, přejděte na stránku **Weby** v nástroji pro tvorbu webu a vyberte **Kopírovat web**. Poté v dialogu **Kopírovat web**, který se objeví, můžete vybrat zdrojový web a zadat název cílového webu.

V tuto chvíli ještě nemůžete vybrat výchozí online kanál a jazyk webu. Tyto vlastnosti však můžete konfigurovat po dokončení operace kopírování webu. Při prvním výběru webu na stránce **Weby** v nástroji pro tvorbu webu se zobrazí dialogové okno **Nastavení vašeho webu**, kde můžete vybrat výchozí kanál a jazyk.

Další informace o kopírování webu naleznete v tématu [Kopírování webu elektronického obchodování](copy-ecommerce-site.md).

### <a name="manage-an-existing-site-channel"></a>Správa stávajícího kanálu webu

Po konfiguraci kanálu webu můžete kanál spravovat a aktualizovat z vybraného webu v nástroji pro tvorbu webu v nabídce **Nastavení webu \> Kanály**, jak je znázorněno na následující ilustraci.

![Správa mapování kanálů v nástroji pro tvorbu webu.](media/channel-mapping-7.png)

## <a name="support-multiple-sites-in-a-single-tenant"></a>Podpora více webů v jednom klientu

Mnoho značkových webů může koexistovat v jediném klientu. Následující příklad ukazuje tři různé značkové weby (Adventure Works, Adventure Works Business a Fabrikam), z nichž každý je namapován na jiný jediný online kanál.

![Seznam webů v nástroji pro tvorbu webu.](media/channel-mapping-8.png)

## <a name="configure-a-single-domain-name-with-paths-for-multiple-sites"></a>Konfigurace názvu jedné domény s cestami pro více webů

Jeden název domény lze použít pro více webů a cesty pak lze použít k oddělení webů nebo jazyků. Například doménu `www.mycompany.com` lze konfigurovat pro dva různé weby elektronického obchodování: jeden pro Fabrikam a jeden pro Adventure Works. V tomto případě lze výchozí cestu (`www.mycompany.com`) použít pro web Fabrikam a jinou cestu (např. `www.mycompany.com/adventureworks`) pro web Adventure Works. Další možností je použít vlastní cestu (např. `www.mycompany.com/fabrikam`) místo výchozí cesty také pro web Fabrikam.

Alternativně lze pro každý web použít jiný název domény (např. `www.adventure-works.com` a `www.fabrikam.com`). Cesty pak lze použít pro různé jazyky nebo oblasti (např. `www.adventure-works.com/fr-ca` pro kanadský web ve francouzštině).

## <a name="configure-multiple-languages-on-a-site"></a>Konfigurace více jazyků na webu

Jazyky online obchodu lze konfigurovat v nástroji pro tvorbu webů v nabídce **Nastavení webu \> Kanály**. V následujícím příkladu byl každý jazyk konfigurován pomocí národního prostředí pro cestu, takže každý jazyk má jedinečnou adresu URL.

![Na webu je konfigurováno několik jazyků.](media/channel-mapping-10.png)

Chcete-li přidat nový jazyk kanálu, přejděte na **Nastavení webu \> Kanály** a vyberte odkaz na kanál. V podokně, které se zobrazí po pravé straně, vyberte **Přidat národní prostředí** a vyberte kanál a národní prostředí, které chcete přidat. Poté zadejte cestu, která se má použít pro vybraný kanál.

### <a name="add-and-configure-the-site-picker-module"></a>Přidání a konfigurace modulu pro výběr webu

Poté, co nakonfigurujete více jazyků nebo kanálů pro web, můžete do záhlaví stránky webu přidat prvek pro výběr jazyka, aby si uživatelé mohli ručně vybrat svůj jazyk nebo zemi. [Modul záhlaví](author-header-module.md) z knihovny modulů má vestavěnou uživatelskou podporu pro výběr jazyka pomocí [modulu pro výběr webu](site-selector.md). Modul pro výběr webu lze přidat do pozice modulu záhlaví ve fragmentu záhlaví.

Další informace o přidání a konfiguraci modulu pro výběr webu naleznete v článku [Modul pro výběr webu](site-selector.md).

### <a name="implement-page-variants-for-each-language"></a>Implementace variant stránek pro každý jazyk

V tomto scénáři existuje pouze jeden kanál, ale více jazyků. Vzhled stránky můžete změnit na základě zvoleného jazyka vytvořením varianty stránky. Do varianty pak můžete přidat lokalizovaný obsah.

Když máte stránku otevřenou v nástroji pro tvorbu webu a vyberete odkaz v pravém horním rohu, který zobrazuje aktuální kanál a jazyk, zobrazí se nástroj pro výběr kanálu a jazyka, jak ukazuje následující příklad. Pokud chcete stránku přepsat pro aktuální jazyk, vyberte jiné národní prostředí a poté vyberte **Změnit**. Kanál můžete také změnit, pokud provádíte [správu webu, který má více kanálů a jazyků](#manage-site-content-that has-multiple-channels-and-languages).

![Změna jazyka stránky v nástroji pro tvorbu webu.](media/channel-mapping-14.png)

Pokud varianta pro vybranou stránku nebo fragment ještě nebyla vytvořena, zobrazí se varovná zpráva, jak ukazuje následující příklad. V tomto případě vyberte odkaz **Vytvořit variantu stránky** v textu zprávy. Dialogové okno, které se zobrazí, nabízí možnosti, které vám umožní buď začít s kopií existující varianty, nebo vytvořit zcela novou stránku ze šablony.

![Výzva k vytvoření varianty stránky v nástroji pro tvorbu webu](media/channel-mapping-16.png)

Pokud nevytvoříte variantu, vykreslí se původní stránka a zobrazí se příslušný jazyk pro řetězce modulů a informace o produktech z centrály Commerce. Pokud však byl text, jako je název stránky nebo jiný marketingový obsah, zadán přímo v modulech výchozí stránky, řetězce pro tento text zůstanou v původním jazyce.

Namísto ručního vytváření každé stránky a fragmentu můžete každou stránku a fragment exportovat do souboru XLIFF (XML Localization Interchange File Format), který pak lze odeslat k lokalizaci. Poté, co byl každý soubor XLIFF přeložen, může být importován jako lokalizovaná varianta stránky. Chcete-li exportovat soubor XLIFF ze stránky nebo fragmentu v nástroji pro tvorbu webu, nebo importovat soubor XLIFF do stránky či fragmentu, vyberte příkaz **Lokalizace** v pruhu příkazů. Poté vyberte buď **Exportovat XLIFF** nebo **Importovat XLIFF**, jak je znázorněno na následujícím obrázku.

![Import nebo export stránky či fragmentu ve formátu XLIFF.](media/channel-mapping-18.png)

## <a name="manage-site-content-that-has-multiple-channels-and-languages"></a>Správa obsahu webu, který má více kanálů a jazyků

Web, který má více kanálů a/nebo jazyků, ukládá jedinečnou variantu každé stránky a fragmentu pro každou kombinaci kanálu a jazyka. Toto chování umožňuje, aby varianty stránky obsahovaly lokalizovaná data, ale také vám poskytuje flexibilitu při změně vzhledu a chování stránky pro konkrétní variantu.

Informace o tom, jak pracovat s variantami stránek, naleznete v sekci [Implementace variant stránek pro každý jazyk](#implement-page-variants-for-each-language) tohoto článku.

## <a name="configure-multiple-channels-on-an-e-commerce-site"></a>Konfigurace více kanálů na webu elektronického obchodu

Kanály můžete do webu elektronického obchodu přidat v nástroji pro tvorbu webu tak, že přejdete na **Nastavení webu \> Kanály** a vyberete příkaz **Přidat kanál**. Poté v dialogovém okně **Přidat kanál** vyberte online kanál a výchozí národní prostředí.

## <a name="additional-resources"></a>Další prostředky

[Přehled kanálů](channels-overview.md)

[Nastavení online kanálu](channel-setup-online.md)

[Přehled organizací a organizačních hierarchií](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md)

[Nastavení geografické detekce a přesměrování](geo-detection-redirection.md)

[Povolení a používání sdílení napříč kanály](cross-channel-sharing.md)

[Vytvoření webu elektronického obchodu](create-ecommerce-site.md)

[Kopírování webu elektronického obchodu](copy-ecommerce-site.md)

[Modul pro výběr lokality](site-selector.md)
