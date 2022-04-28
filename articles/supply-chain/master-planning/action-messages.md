---
title: Zprávy akce
description: Zpráva opatření je návrh vygenerovaný systémem na změnu existující plánované nebo potvrzené objednávky.
author: t-benebo
ms.date: 03/18/2022
ms.topic: article
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: e6df6cfd038383b3eeaa3659e0af3e469429f81e
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570247"
---
# <a name="action-messages"></a>Zprávy akce

[!include [banner](../includes/banner.md)]

Zpráva opatření je návrh vygenerovaný systémem na změnu existující plánované, schválené nebo potvrzené objednávky.

Zprávy akcí jsou generovány při výpočtu hlavního plánování jako reakce na změněné požadavky. Na prodejní objednávce, pro kterou jste již vytvořili nákupní objednávku, se mění například datum expedice nebo množství, aby byl splněn požadavek pro danou prodejní objednávku. V tomto případě se při výpočtu hlavního plánování vygeneruje jedna nebo více zpráv akcí, které navrhují aktualizovat nákupní objednávku. Můžete se rozhodnout, zda navržené změny provést.

Můžete nastavit způsob, jakým se zprávy akcí vypočítávají pro skupinu disponibility, kterou připojíte k položce.

## <a name="select-action-messages"></a>Výběr zpráv akcí

Na stránce **Skupiny disponibility** můžete vybrat zprávy akcí, které má sytém vygenerovat, a skupiny disponibility nebo položky, na které se mají zprávy použít. V následující tabulce jsou uvedeny zprávy akcí, které můžete vybrat.

| Zpráva | Popis |
|---|---|
| Posunout | Systém dle potřeby vygeneruje zprávy akcí, aby se objednávka přesunula na dřívější datum. V poli **Doba posunutí** můžete nastavit maximální počet dní mezi příjmem a výdejem bez posunutí. |
| Odložit | Systém dle potřeby vygeneruje zprávy akcí, aby se objednávka přesunula na pozdější datum. V poli **Doba odkladu** můžete nastavit také maximální počet dní, které mohou uplynout mezi příjmem a výdejem bez odkladu. |
| Snížení | Systém vygeneruje zprávy akcí, když by se měly výrobní zakázky, nákupní objednávky a jiné příjmové transakce snížit tak, aby se zabránilo přebytku zásob. |
| Zvýšit | Systém vygeneruje zprávy akcí, když by se měly výrobní zakázky, nákupní objednávky a jiné příjmové transakce zvýšit tak, aby se zabránilo nedostatku zásob. |
| Odvozené akce | Zprávy o akcích, které jsou vytvořeny pro transakce příjmu, budou rozšířeny na všechny odvozené požadavky a pro transakce příjmu, které tyto požadavky splňují, budou generovány zprávy o nezbytných akcích. |

V následujících sekcích je uvedeno několik podrobných scénářů.

## <a name="increase-and-decrease-actions-with-product-default-order-quantities"></a>Zvyšte a snižte akce s výchozím objednávkovým množstvím produktu

Na stránce **Výchozí nastavení objednávky** pro položku můžete nastavit minimální množství objednávky, maximální množství objednávky a více hodnot. Systém pak tato nastavení bere v úvahu, když navrhuje akce, aby zajistil, že návrhy nikdy nezpůsobí nedostatek zásob.

Máte například položku, která má na sobě následující nastavení na stránce **Výchozí nastavení objednávky**:

- **Minimální množství objednávky:** *0*
- **Maximální množství objednávky:** *90*
- **Násobek:** *20*

Pokud je poptávka po množství 60 kusů této položky, hlavní plánování vytvoří plánovanou nákupní objednávku na množství 60. Pokud se poptávka zvýší o 30, hlavní plánování navrhne zvýšení o 40, protože bude respektovat násobek 20 a nikdy nezpůsobí nedostatečnou nabídku.

## <a name="action-messages-for-orders-related-to-safety-stock"></a>Akční zprávy pro objednávky týkající se bezpečnostních zásob

Akční zprávy pro objednávky, které dodávají bezpečnostní zásoby, nikdy nenavrhnou snížit množství pod množství, které je potřebné pro bezpečnostní zásoby. Jinými slovy, pokud existuje objednávka, která dodává bezpečnostní zásoby a poptávku zákazníků, a poptávka je snížena nebo zrušena, hlavní plánování navrhne snížení plánované objednávky o sníženou poptávku. Nikdy však nenavrhne hodnotu, která je nižší než potřebná bezpečnostní zásoba.

Systém nenavrhne odložení akcí pro dodání bezpečnostní zásoby, protože se předpokládá, že bezpečnostní zásoba musí být dodána v požadovaném čase a v požadovaném termínu.

### <a name="advance-and-postpone-actions-related-to-boms"></a>Posuňte a odložte akce související s kusovníky

Akce, které souvisejí s komponentami kusovníků (BOM), musí být aplikovány před akcemi jejich nadřazených položek, protože mohou být ovlivněny další objednávky, které souvisejí s kusovníky vyšší úrovně. Poté musíte znovu spustit hlavní plánování, abyste přepočítali a navrhli vhodná opatření.

Například máte následující situaci:

- Konečné zboží *FG* typu *výroba* má kusovník, který obsahuje surovinu *RM*.
- Dnešní datum je 21. ledna.
- Existující uvolněná výrobní zakázka pro *FG* je naplánován na 25. ledna.
- Pro podporu stávající výrobní zakázky hlavní plánování vytvořilo plánovanou nákupní objednávku na požadovanou surovinu *RM*. Tato objednávka má datum požadavku 25. ledna.
- Nová prodejní objednávky pro *FG* se vytvoří dnes. Má dnešní datum požadavku (21. leden).
- 21. ledna je zavřeno pro doručení v kalendáři *RM*, ale 22. ledna je otevřeno.

Když je spuštěno hlavní plánování, generuje předběžné akční zprávy, které navrhují přesunout dříve naplánovanou výrobu nahoru, abyste mohli splnit dnešní objednávku.

- Pro uspokojení nové poptávky navrhuje přesunutí výrobní zakázky *FG* na 21. ledna. (Tento návrh činí bez ohledu na datum uzavření *RM*.)
- Protože *RM* je stále vyžadován pro výrobní objednávku, navrhuje také posunout plánovanou nákupní objednávku nahoru. Tentokrát však zkontroluje kalendář *RM*. Proto navrhuje přesunout plánovanou objednávku *RM* na 22. ledna (protože 21. ledna je zavřeno).

Jak vidíte, požadovaná surovina *RM* nyní dorazí příliš pozdě na plánovanou výrobu *FG*. Proto musíte nejprve použít akci posunutí plánované nákupní objednávky pro *RM* a poté znovu spusťte hlavní plánování. V tomto okamžiku hlavní plánování vygeneruje novou akční zprávu, která navrhuje přesunutí výrobní zakázky *FG* na 22. ledna.
