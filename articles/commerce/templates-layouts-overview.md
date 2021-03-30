---
title: Přehled šablon a rozvržení
description: Toto téma popisuje šablony a rozvržení v aplikaci Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 12/12/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 319e60f34c7e94cc56386b0f86ac83360f7b0456
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232584"
---
# <a name="templates-and-layouts-overview"></a>Přehled šablon a rozvržení


[!include [banner](includes/banner.md)]

Šablony představují základní prvek modelu stránek Microsoft Dynamics 365 Commerce. Pokud chcete maximalizovat efektivitu a konzistenci pracovních postupů pro vytváření webů, je důležité, abyste se dozvěděli, jak pořizovat výhody šablon vašeho webu. Brzká rozhodnutí o struktuře šablon jsou důležitá a mohou významně ovlivnit náklady a pružnost denních a sezónních aktualizací značek pro celý web. Dobře strukturované šablony mají také jiné výhody. Mohou například pomoci zdokonalit výsledky optimalizace vyhledávače pro celou lokalitu (SEO) a minimalizovat počet chyb.

Dobrým prostředkem pro práci se šablonami je pochopení funkčních přínosů šablon a rozvržení, jejich rozdílů a hierarchie.

Následující ilustrace znázorňuje hierarchii modelu stránky za zobrazenou webovou stránkou.

![Diagram modelu stránky](../commerce/media/page-model-diagram.png)

| Celek        | Základní funkce |
|---------------|----------------|
| Šablona      | Šablony definují možnosti modulu a základní generování uživatelského rozhraní pro sadu rozložení a instancí stránky. |
| Rozložení        | Rozložení definují konečný výběr a uspořádání modulů pro stránku nebo sadu stránek. |
| Instance stránky | Instance stránky definují data a obsah pro konkrétní stránky. |

## <a name="templates"></a>Šablony

Šablony jsou v horní části hierarchie modelu stránky Dynamics 365 Commerce a představují důležitý předběžný krok pro konfiguraci webu. Šablony v principu umožňují konzistenci ovládacích prvků pro celou řadu podřízených rozložení a stránek definováním základní struktury a možností vytváření obsahu pro vytváření rozložení a pracovních postupů vytváření stránek. Šablony mohou zjednodušit proces tvorby obsahu pomocí předdefinovaných, centrálně spravovaných prvků (jako jsou například záhlaví a zápatí) a s vodicími vývojovými toky, které pomáhají zaručit, že volby konfigurace modulu jsou na značce.

### <a name="controlling-consistency"></a>Kontrola konzistence

Při návrhu šablony je největší obchodní rozhodnutí, které je nutné učinit, jakým způsobem má být šablona kontrolu nad procesem vytváření stránky. Šablona, která ponechává vše otevřené pro navazujícího autora, je nejjednodušší typ šablony na vytvoření, ale může mít dlouhodobé následky na údržbu stránek, které z ní byly vytvořeny. Správně zapsaná šablona poskytuje návod a moderní prostředí pro tvorbu, ale také uživatelům dává dostatečnou flexibilitu, takže mohou dokončit svůj úkol. Všechna tato hlediska závisejí na úrovni řízení, kterou šablona uplatňuje.

Šablony mohou autoři obsahu pomoci efektivněji a zůstat na vašem místě v následujících ohledech:

- Omezte počet modulů, které lze použít na stránce.
- Navrhněte možnosti výchozího modulu a konfigurace.
- Explicitně proveďte některé volby modulu a konfigurace, které jsou řízeny na úrovni šablony. Tento proces se také nazývá *uzamčení* nastavení.

V následujícím příkladu je ukázáno, jak lze konfigurovat základní šablonu (šablonu X):

- Všechna podřízená rozložení šablony X musí mít kontejner záhlaví, kontejner textu a kontejner zápatí.
- Konfigurace kontejneru záhlaví v šabloně X je uzamčena a lze ji změnit pouze v samotné šabloně X. Toto záhlaví mají vždy všechna podřízená rozložení a stránky.
- Kontejner obsahu vyžaduje alespoň jeden modul a nejvýše deset modulů. Tyto moduly jsou definovány rozloženími a stránkami pro příjem dat.
- Pro kontejner obsahu jsou k dispozici moduly typu Hero, funkcí, karusel a banner.
- Kontejner zápatí je konfigurován v šabloně X, ale může být přepsán pro navazující rozložení a stránky.

Šablona v tomto příkladu definuje jednoduchou strukturu a sadu možností pro navazující autory obsahu. Všimněte si, že některé části stránky (v tomto případě záhlaví) jsou plně definovány a uzamčeny v šabloně a nemohou je měnit autoři. Ostatní díly (v tomto případě obsah) mohou být definovány pro navazující autory v rámci zvláštních pokynů (v tomto případě minimální počet a maximální počet modulů specifických typů). Další části (v tomto případě zápatí) jsou definovány v šabloně, ale mohou být přepsány autory.

Důležitým počátečním krokem pro správce webů a obchodních značek je určení správné rovnováhy mezi omezeními a pružností pro podřízené rozložení a autory stránek. Při použití šablon je tato rovnováha zcela konfigurovatelná. Ovlivňuje, zda jsou prvky stránky centrálně aktualizovány (uzamčeny v šabloně) nebo vlevo na úrovně jednotlivých podřízených úrovní, které jsou v hierarchii stránek nižší.

Chcete-li začít používat šablony, [pracujte se šablonami](work-with-templates.md).

## <a name="layouts"></a>Rozložení

Rozvržení jsou následující úrovně v hierarchii modelů stránek pod šablonami. Vzhledem k tomu, že šablona definuje všechny moduly, které jsou povoleny pro určitou stránku, rozložení je explicitním výběrem a uspořádáním modulů. Stránky jsou následující úrovně v hierarchii modelů stránek pod rozvrženími. Definují lokalizované obsahy pro moduly vybrané v rozvržení.

Následující příklad sestaví příklad šablony z předchozího oddílu a ukazuje, jak lze konfigurovat základní rozvržení:

- Nadřazená šablona rozvržení vyžaduje, aby kontejner textu měl mezi jedním až deseti moduly. Tyto moduly mohou být pouze Hero, funkce, karusel a banner. Rozvržení tedy může definovat následující výběr a uspořádání modulů:

    - První modul v kontejneru textu je skládaný modul, následovaný Hero modulem a dvěma moduly funkcí.
    - První modul funkce je zarovnán doleva a druhý modul funkce je zarovnán doprava.

- I když je výchozí zápatí zděděno od nadřazené šablony, autor šablony nechal zápatí odemčeno. Proto může toto rozvržení přepsat definováním jiného fragmentu zápatí.

Rozvržení v tomto příkladu definuje konečné uspořádání modulů pro podřízené stránky. Podobně jako šablona může rozvržení definovat výchozí nebo uzamčené vlastnosti modulu, které budou vždy zděděny podřízenými stránkami (například zarovnání modulů funkcí). Skutečný obsah nebo data pro všechny moduly v rozvržení je pak definováno dále než hierarchie v každé podřízené instanci stránky. Důležitým rozdílem je to, že rozložení neobsahují přímo obsah lokalizovatelné stránky, zatímco jejich podřízené stránky ano. Primární funkce rozložení slouží k definování finálního uspořádání a výchozí konfigurace modulů pro jeho podřízené stránky.

Tato hierarchie je účinná ze dvou důvodů. Zaprvé, rozvržení, která sdílejí stejnou nadřazenou šablonu, jsou považována za kompatibilní pro scénáře přepínání rozvržení. Proto lze rozložení pro libovolnou stránku změnit na jiné rozložení ze stejné hierarchie šablony, aniž by bylo nutné znovu vytvářet obsah na úrovni stránky. Tuto schopnost můžete využít k provádění sezónních aktualizací návrhu, experimentování nebo provádění trvalého přemístění webu. Zadruhe, rozložení poskytují další možnost centrálně upravovat sdílené prvky pro skupinu stránek bez nutnosti aktualizace jednotlivých stránek. Pokud například kategorie produktů obsahuje 1 000 stránek, které sdílejí stejné rozvržení, lze tyto moduly uspořádat v rozvržení a tato změna se ihned projeví ve všech 1 000 podřízených stránkách.

Pochopíte-li tuto hierarchii, můžete dodat agilní a efektivní strukturu pracoviště, která pomáhá ušetřit náklady, je škálovatelná a produkuje lepší výsledky, protože se pracoviště v průběhu času vyvíjí.

### <a name="preset-and-custom-layouts"></a>Přednastavená a vlastní rozvržení

Rozvržení na vašem webu mohou být *přednastavená* nebo *vlastní*:

- **Přednastavená rozložení** umožňují workflow vytvoření stránky, kde jsou všechny moduly již vybrány a uspořádány a jsou požadovány pouze datové položky. Tento přístup vám může pomoci ušetřit čas v případě, že je nutné, aby více stránek vytvořilo stejné požadavky na rozvržení. Přednastavená rozvržení mají vztah 1:n s podřízenými stránkami. Z tohoto důvodu lze použít jediné přednastavené rozložení pro centrální řízení uspořádání modulů pro stovky nebo tisíce podřízených stránek.
- **Vlastní rozložení** jsou v podstatě rozložení s jedním použitím, která jsou vložena na jednu stránku. Nejsou přístupné jako možnost při vytvoření dalších nových stránek nebo ve scénářích přepínání rozvržení. Výhodou tohoto přístupu je, že se autor může experimentovat se stránkou, která používá vlastní rozložení. Pokud pak autor chce rozložení znovu použít pro ostatní stránky, lze jej snadno převést na přednastavené rozložení. Nové přednastavené rozvržení je pak vystaveno jako možnost pro pracovní postupy vytvoření stránky a pro stránky ze stejné hierarchie šablon ve scénářích přepínání rozvržení. Naopak, přednastavená rozložení lze rozdělit do vlastních rozložení. Tímto způsobem může autor rozdělit stránku od přednastaveného rozvržení a vytvořit nové vlastní rozvržení s jedním použitím. (Toto nové vlastní rozložení je stále vázáno libovolnými omezeními v nadřazené šabloně.)

Přednastavené rozvržení a vlastní rozvržení jsou upravovány v různých částech sady nástrojů pro vytváření. Vzhledem k tomu, že vlastní rozložení nemají žádné závislosti na jiných stránkách, jsou upravována přímo v editoru stránek. V tomto případě je existence rozvržení převážně transparentní pro uživatele a je vystavena pouze ve vlastnostech na úrovni stránky a pomocí akcí pro možnosti rozložení. Vzhledem k tomu, že změny rozvržení přednastavených prvků mohou ovlivnit mnoho podřízených stránek, je nutné je upravit v editoru rozložení, kde akce publikování posuzují úplný dopad na podřízené stránky.

Následující ilustrace zobrazuje scénáře pro přednastavená a vlastní rozložení.

![Přednastavené a vlastní scénáře rozložení](../commerce/media/template-figure1.png)

Chcete-li začít používat přednastavená rozvržení, postupujte podle [Práce s přednastavenými rozvrženími](work-with-layouts.md).

## <a name="additional-resources"></a>Další zdroje

[Práce se šablonami](work-with-templates.md)

[Práce s přednastavenými rozloženími](work-with-layouts.md)

[Práce se skupinami publikování](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]