---
title: Správa sortimentu
description: Toto téma vysvětluje základní koncepty správy sortimentu v aplikaci Dynamics 365 Commerce a poskytuje úvahy nad implementací pro váš projekt.
author: jblucher
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: Global
ms.author: jeffbl
ms.search.validFrom: 2017-11-21
ms.dyn365.ops.version: Application update 5
ms.openlocfilehash: a81a779dd484d30397c89076d081413a72560f0b
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348700"
---
# <a name="assortment-management"></a>Správa sortimentu

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Přehled

Dynamics 365 Commerce nabízí *sortimenty*, které umožňují spravovat dostupnost produktu mezi kanály. Sortimenty určují, které produkty jsou k dispozici v konkrétních obchodech a v konkrétním období.

V aplikaci Commerceje sortiment mapováním jednoho nebo více kanálů (nebo skupin kanálů při použití hierarchií organizace) na jeden nebo více produktů (nebo skupin produktů, pokud jsou použity hierarchie kategorií).

Celková kombinace produktu kanálu je určena publikovanými sortimenty, které jsou přiřazeny ke kanálu. Proto můžete konfigurovat více aktivních sortimentů na jeden kanál.

### <a name="basic-assortment-setup"></a>Nastavení základního sortimentu

V následujícím příkladu je nakonfigurován jedinečný sortiment pro každý obchod. V takovém případě je pouze produkt 1 k dispozici v obchodě 1 a pouze produkt 2 je k dispozici v obchodě 2.

![Každý produkt je k dispozici v jednom obchodě.](./media/Managing-assortments-figure1.png)

Chcete-li, aby byl produkt 2 k dispozici v obchodě 1, lze přidat produkt do sortimentu 1.

![Produkt 2 přidán do sortimentu 1.](./media/Managing-assortments-figure2.png)

Případně můžete přidat obchod 1 do sortimentu 2.

![Obchod 1 přidán do sortimentu 2.](./media/Managing-assortments-figure3.png)

### <a name="organization-hierarchies"></a>Organizační hierarchie

V situacích, kdy více kanálů sdílejí stejné sortimenty produktů, můžete nakonfigurovat sortimenty pomocí hierarchie organizace sortimentu aplikace Commerce. Při přidávání uzlů z této hierarchie budou zahrnuty všechny kanály v tomto uzlu a jeho podřízené uzly.

![Organizační hierarchie.](./media/Managing-assortments-figure4.png)

### <a name="product-categories"></a>Kategorie produktu

Stejně tak na straně produktu můžete zahrnout skupiny produktů pomocí hierarchie kategorií produktu. Můžete konfigurovat sortimenty zahrnutím jednoho nebo více uzlů hierarchie kategorií. V tomto případě bude sortiment obsahovat všechny produkty v tomto uzlu kategorie a jeho podřízených uzlech.

![Kategorie produktu.](./media/Managing-assortments-figure5.png)

### <a name="excluded-products-or-categories"></a>Vyloučené produkty nebo kategorie

Kromě zahrnutí produktů a kategorií do sortimentů můžete použít možnost Vyloučit pro definování specifických produktů nebo kategorií, které mají být vyloučeny ze sortimentů. V následujícím příkladu chcete zahrnout všechny produkty do specifické kategorie, kromě produktu 2. V takovém případě nemusíte definovat produkt sortimentu podle produktu nebo vytvořit další uzly kategorie. Místo toho můžete pouze zahrnout kategorii, ale vyloučit produkt.

> [!NOTE]
> Pokud je produkt současně zahrnut a vyloučen v jednom nebo více sortimentech podle svojí podstatou, produkt bude vždy považován za vyloučený.

![Vyloučené produkty.](./media/Managing-assortments-figure6.png)

### <a name="global-and-released-products"></a>Globální a uvolněné produkty

Sortimenty definované na úrovni globálního a může obsahovat kanálů z více právnických osob. Produkty a kategorie, které jsou zahrnuty v sortimentech, jsou také sdíleny mezi právnickými osobami. Produkt je však nutné uvolnit předtím, než ho lze prodat, objednat, spočítat nebo přijmout v daném kanálu (například v pokladním místě \[POS\]). Přestože dva obchody v různých právnických osobách mohou sdílet sortiment obsahující stejné produkty, produkty jsou k dispozici pouze v případě, že byly uvolněny do těchto právnických osob.

### <a name="dynamic-and-static-assortments"></a>Dynamické a statické sortimenty

Sortimenty mohou být definovány konkrétními kanály a produkty, nebo zahrnutím organizačních jednotek a kategorií. Sortimenty včetně odkazů na tyto skupiny jsou považovány za dynamické sortimenty. Pokud se definice nebo obsah těchto skupin změní, když je sortiment aktivní, změní se také definice sortimentu.

Například sortiment je původně definován a publikován, takže odkazuje na kategorii produktů. Jsou-li později přidány další produkty do kategorie, jsou tyto produkty automaticky zahrnuty v definici existujícího sortimentu. Nemusíte přidávat ručně produkty do sortimentu. Pokud je obdobným způsobem přidána organizační jednotka do jiné uzlu, sortiment organizační jednotky se automaticky upraví na základě dané definice.

### <a name="stopped-products"></a>Zastavené produkty

Můžete "zastavit" uvolněné produkty pro prodejní proces zapnutím nastavení v nastavení **Výchozí objednávka**. Toto nastavení se nejčastěji používá, když je produkt na konci životnosti a neměl by se prodávat na žádném kanálu. Sortimenty respektují toto nastavení a zastavené produkty nebudou roztříděny, bez ohledu na konfiguraci sortimentu.

### <a name="blocked-products"></a>Blokované produkty

Kromě zastavení prodeje produktů je možné blokovat dočasně prodej produktu. Toto nastavení lze konfigurovat na kartě **Commerce** uvolněného produktu. Blokované produkty jsou stále roztříděny, ale obdržíte zprávu v pokladním místě, která uvádí, že produkt nelze prodávat.

### <a name="date-effectivity"></a>Platnost od

Sortimenty mají časovou platnost. Proto mohou maloobchodní prodejci nakonfigurovat, kdy mají nebo nemají být produkty k dispozici pro kanál. Můžete definovat a publikovat sortimenty předem a určit počáteční a koncová data. Produkty budou automaticky dostupné nebo nedostupné v určených datech.

### <a name="process-assortments-batch-job"></a>Zpracování dávkové úlohy sortimentu

Sortimenty definované v aplikaci Commerce je nutné zpracovat předtím, než začnou platit. Toto zpracování se provede z následujících důvodů:

- Definice sortimentu musí být denormalizované, aby je mohly kanály snadněji spotřebovat. Kombinaci produktů pro kanál lze definovat pomocí více sortimentů, které přesahují různé datové rozsahy. Když je některá z těchto informací vypočítána předem na serveru, zlepší se výkonnost na daném kanálu.
- Produkty a kanály v sortimentu lze změnit mimo samotný sortiment. Dynamické sortimenty, které obsahují odkazy na kategorie nebo organizační jednotky, musí být zpracovány pravidelně tak, aby zahrnovaly nebo vylučovaly záznamy podle jejich aktuálního přiřazení.

## <a name="implementation-considerations"></a>Na co myslet při implementaci

Když plánujete a spravujete sortimenty pro svou maloobchodní implementaci, zvažte následující požadavky na implementaci Commerce:

- **Replikace dat a velikost databáze** – Ačkoli sortimenty pomáhají sloužit obchodním potřebám pro správu dostupnosti produktu, jsou také důležitým nástrojem pro správu velikosti kanálu a offline databází. Správně spravované sortimenty pomáhají snížit množství dat, které musí být zpracováné a replikované do kanálu a offline databází. Pomáhají také snížit počet záznamů, které musí být trvalé. Méně záznamů v těchto databázích zvýší výkonnost při přidání položek do transakce, hledání a procházení produktů.
- **Platné/vypršené sortimenty** – Jedním z nejúčinnějších nástrojů pro správu počtu produktů v kanálu a offline databázích je datum platnosti sortimentu. Pokud ponecháte s otevřeným koncem (bez vypršení) sortimenty pro sezónní produkty nebo produkty na konci životnosti, databáze bude růst nekonečně. K zvládnutí této situace můžete použít různé přístupy. Například můžete udržovat samostatné sortimenty sezónních produktů a produktů, které jsou vždy k dispozici.
- **Prodeje a vrácení mimo sortimenty** – Tato možnost pomáhá maloobchodním prodejcům efektivně spravovat své sortimenty pomocí omezení počtu dostupných produktů na produkty, které patří do základní kombinace produktů obchodu. Tato funkce také pomáhá maloobchodním prodejcům zvládat situace, kdy byl produkt omylem vynechán ze sortiment nebo kdy byl vrácen mimo data platnosti sortimentu.

Pokud v databázi kanálů neexistují data produktů, pokladní místo provádí volání v reálném čase do centrály pro načtení požadovaných informací, aby mohl být produkt prodán, vrácen nebo umístěn na objednávku odběratele. Informace o produktu, které jsou tímto způsobem načteny, jsou k dispozici pouze v rozsahu dané transakce. Produkt není přidán do definice sortimentu. Proto budou následující volání v reálném čase provedena podle potřeby.


[!INCLUDE[footer-include](../includes/footer-banner.md)]