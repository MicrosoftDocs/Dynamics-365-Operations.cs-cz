---
title: Práce se skupinami publikování
description: Toto téma popisuje funkci skupin publikování v aplikaci Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b623573f598f6b21291cafe95fa04e6777cffe11
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244832"
---
# <a name="work-with-publish-groups"></a>Práce se skupinami publikování


[!include [banner](includes/banner.md)]

Toto téma popisuje funkci skupin publikování v aplikaci Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Přehled

Internetové stránky E-commerce jsou průběžně aktualizovány novým obsahem po celý rok. Aktualizace jsou často publikovány v dávkách kolem zaneprázdněných událostí E-commerce, jako jsou svátky, sezónní marketingové kampaně nebo propagační akce. Tyto aktualizace často vyžadují, aby byly skupiny obsahu webu (příklady, stránky, obrázky, fragmenty a šablony) připraveny, ověřeny a publikovány souběžně v jedné akci.

Možnost seskupit položky do logických množin, které společně publikují položky, kde každá sada má svůj vlastní životní cyklus, poskytuje pro autory webů mnoho výhod. V Commerce se tyto logické množiny nazývají skupiny publikování. Autoři webu umožňují autorům webů sledovat sady aktualizací jako vlastní konfigurovatelné, testovatelné a publikovatelné entity.

Autoři mohou zobrazit náhled aktualizací v připravené skupině publikování, aniž by ovlivnili živý web nebo jiné samostatné publikované skupiny. Autoři pak mohou naplánovat akci publikování tak, aby současně publikovali všechny položky ve skupině publikování na webu v ostrém provozu. Možnost seskupit, zobrazit náhled a naplánovat aktualizace pro publikování je důležitá pro mnoho společností na úrovni organizace, které generují značné roční výnosy kolem milníků aktualizace webu založeného na událostech.

Společnosti mohou vynakládat náklady na pomalé nebo neověřené efekty obsahu, které nejsou plynulé. Skupiny publikování pomáhají zaručit, že spuštění bude uspořádáno, ověřeno a publikováno včas. Bez ohledu na to, zda se jedná o skupiny velké nebo malé, poskytují skupiny pro publikování cennou sadu nástrojů, která pomáhá autorům organizovat a zjednodušit probíhající úlohy aktualizace webu.

## <a name="when-to-use-publish-groups"></a>Kdy použít skupiny publikování

Skupiny publikování lze použít vždy, když je nutné sestavit a publikovat více dokumentů najednou. Pokud například web aktualizuje obsah každou sezónu, můžete vytvořit skupiny publikování pro tyto sezónní marketingové pohyby. Vaše publikační skupina "Podzimní sezónní aktualizace" může obsahovat nové sezónní obrazy, fragmenty, které mají sezonní marketingové zprávy, stránky obsahující sezonní sbírky produktů nebo jiné sezonní aktualizace webu.

Výhodou publikovaných skupin je, že můžete souběžně aktualizovat více aktualizací. Například brzy po aktualizaci skupiny pro publikování "Podzimní sezónní aktualizace" může dojít k aktualizaci obsahu pro konkrétní prázdninový víkend. V tomto případě můžete obsah skupiny pro publikování "Podzimní sezónní aktualizace" upravit současně s obsahem pro následující publikovou skupinu "Podzimní sváteční aktualizace". Každá skupina publikování obsahuje vlastní jedinečnou sadu stránek, obrázků, fragmentů, šablon atd. Tyto dvě skupiny publikování můžete zobrazit, prohlédnout a ověřit nezávisle, ale na souběžné časové ose. U každé skupiny publikování lze potom naplánovat přechod na web v určitých datech a časech.

## <a name="turn-on-the-publish-groups-feature"></a>Zapnutí funkce skupin publikování

Funkce skupin publikování je volitelná a musí být pro váš web zapnuta.

Chcete-li zapnout funkci skupin publikování pro web v nástrojích pro vytváření obchodních dokumentů, postupujte takto.

1. V levém navigačním podokně vyberte **Nastavení webu** a rozbalte je.
1. V části **nastavení webu** vyberte **Funkce**.
1. Nastavte možnost **Skupiny publikování** na **Zapnuto**.

## <a name="create-a-publish-group"></a>Vytvoření skupiny publikování

Chcete-li vytvořit skupinu publikování pro web ve vývojových nástrojech Commerce, postupujte takto.

1. V levém navigačním podokně nalevo vyberte položku **Skupiny publikování**.
1. Na horním příkazovém řádku vyberte možnost **Nový**.
1. V dialogovém okně **Vytvořit skupinu publikování** v části **název skupiny publikování** zadejte popisný název. Pak vyberte **OK**.

## <a name="set-the-publish-group-authoring-context"></a>Nastavit kontext vytváření skupin publikování

V Commerce je výchozím vývojovým kontextem kontext živého webu. Aktivní kontext pro vytváření webů je výchozí zobrazení, ve kterém můžete zobrazit a provádět změny přímo na webu bez použití skupiny publikování. Představuje nejnovější přímé aktualizace publikované verze webu. Pokud ovládací prvek kontextu v **Skupiny publikování** v levém navigačním podokně zobrazuje název **Aktivní web**, pracujete v kontextu vytváření živého webu. **Aktivní web** je výchozí název kontextového ovládacího prvku. V opačném případě zobrazí ovládací prvek kontextu název skupiny publikování.

Chcete-li pracovat ve skupině publikování, musíte pro ni přepnout na kontext vytváření. Chcete-li nastavit kontext skupiny publikování, postupujte podle jednoho z následujících kroků.

- V levém navigačním podokně vyberte kontextový ovládací prvek přímo v části **Skupiny publikování** a pak vyberte název skupiny publikování v seznamu možností, které se zobrazí. Ovládací prvek kontextu je přejmenován a zobrazí název skupiny publikování.
- V levém navigačním podokně vyberte položku **Skupiny publikování** a potom v části **Skupiny publikování** vyberte název skupiny publikování. Ovládací prvek kontextu je přejmenován a zobrazí název skupiny publikování.

Po nastavení kontextu vytváření skupiny publikování pracujete v tomto kontextu skupiny publikování při zobrazení náhledu a úpravě obsahu webu.

Chcete-li se vrátit k výchozímu kontextu pro vytváření živého webu, vyberte ovládací prvek kontextu a pak vyberte **Aktivní web**.

## <a name="add-pages-or-other-items-to-a-publish-group"></a>Přidání stránek nebo jiných položek do skupiny publikování

Jakmile vyberete kontext pro vytváření skupin publikování a ovládací prvek kontextu v levém navigačním podokně zobrazí jeho název, můžete vytvořit obsah stejně jako ve výchozím kontextu živého webu. Můžete také přidat existující stránky nebo jiné položky z jiných skupin publikování nebo z kontextu živého webu.

Chcete-li zkopírovat existující stránky do skupiny publikování, postupujte následovně.

1. Vyberte vývojový kontext, ze kterého chcete kopírovat, a pak v levém navigačním podokně vyberte **Stránky**.
1. Vyberte stránku, kterou chcete přidat do skupiny publikování.
1. Na panelu příkazů vyberte možnost **Kopírovat do skupiny publikování**.
1. V dialogovém okně **Vybrat skupinu publikování** vyberte skupinu publikování, do které chcete stránku přidat, a pak vyberte **OK**.

Stejné základní kroky můžete použít k vytvoření přizpůsobených stránek produktu, adres URL, šablon, rozložení, fragmentů a datových zdrojů knihovny médií nebo k přidání existujících položek těchto typů do skupiny publikování.

## <a name="validate-a-publish-group"></a>Ověření skupiny publikování

Chcete-li zajistit, aby všechny závislosti v obsahu skupiny publikování byly splněny a aby byla předána všechna ověření, můžete spustit ověřování a identifikovat problémy, které je třeba vyřešit před naplánováním akce publikování.

Chcete-li ověřit skupinu publikování před jejím naplánovali, postupujte takto:

1. V levém navigačním podokně nalevo vyberte položku **Skupiny publikování**.
1. Vyberte skupinu publikování k ověření.
1. Na příkazovém řádku vyberte možnost **Ověřit**.

Ověřování je spuštěno u veškerého obsahu ve skupině publikování. Všechny problémy, které zabrání úspěšnému přijetí akce publikování, jsou zobrazeny v oznamovací oblasti, která se zobrazí v pravém horním rohu okna.

> [!NOTE]
> Ověřování je vždy spuštěno automaticky při plánování skupiny publikování. Tlačítko **Ověření** na panelu příkazů je však užitečné, protože pomáhá identifikovat problémy, které je nutné opravit, než se pokusíte naplánovat skupinu publikování pro ostrý provoz.

## <a name="schedule-a-publish-group-to-go-live"></a>Plánování skupiny publikování pro přechod na ostrý provoz

Chcete-li naplánovat, aby skupina publikování na vašem webu přešla do ostrého provozu, postupujte takto.

1. V levém navigačním podokně nalevo vyberte položku **Skupiny publikování**.
1. V sekci **Skupiny publikování** vyberte skupinu publikování, kterou chcete naplánovat.
1. Na příkazovém řádku vyberte možnost **Upravit plán**. Zobrazí se dialogové okno **Upravit plán**.
1. Vyberte datum a čas, kdy má skupina publikování přejít na ostrý provoz, a pak klepněte na **OK**.

Chcete-li zrušit naplánování skupiny publikování, postupujte podle stejných kroků, ale vyberte **Zrušit plánování skupiny publikování** v dialogovém okně **Upravit plán**.

> [!NOTE]
> Velké skupiny publikování mohou trvat až dvě minuty, než budou publikovány. Uvědomte si, že akce publikování není okamžitá a že menší skupiny publikování budou publikovány rychleji.

## <a name="publish-groups-faq"></a>FAQ skupin publikování

**Kolik položek může být ve skupině publikování?**

V současné době existuje limit 2 000 položek na jednu skupinu publikování. Uvědomte si, že velmi velkým skupinám publikování může trvat až dvě minuty, než budou publikovány.

**Jsou skupiny publikování jako kódové "větve" v terminologii vývoje softwaru?**

Ano i ne. Skupiny publikování lze považovat za rozvětvené verze webu. Tímto způsobem se chovají jako větve. Neexistuje však koncept sloučení na úrovni jednotlivých položek. Položka, která byla publikována jako poslední, pouze přepíše, co dříve existovalo, a poslední akce publikování vždy nahrazuje předchozí akce publikování.

**Je možné naplánovat dvě skupiny publikování tak, aby byly zveřejněny ve stejné době?**

Č. Z důvodu výkonu a konfliktů vám systém vynutí nastavit naplánované skupiny publikování alespoň pět minut od sebe.

**Je možné pomocí skupin publikování naplánovat multikanálové administrativní položky, jako jsou slevy a aktualizace produktů?**

Funkce skupin publikování v současné době podporuje pouze obsah webu. Společnost Microsoft si je však vědoma toho, že integrace s administrativními scénáři prodeje by mohla být užitečná pro koordinaci a automatizaci spouštění kampaně omnikanálů.

## <a name="additional-resources"></a>Další zdroje

[Způsoby přidání obsahu](add-manage-content.md)

[Glosář modelu stránky](page-elements-overview.md)

[Stavy dokumentu a životního cyklu](document-states-overview.md)

[Povolení a používání sdílení napříč kanály](cross-channel-sharing.md)

[Práce s moduly](work-with-modules.md)

[Práce s fragmenty](work-with-fragments.md)

[Přehled šablon a rozvržení](templates-layouts-overview.md)

[Přizpůsobení navigace na webu](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]