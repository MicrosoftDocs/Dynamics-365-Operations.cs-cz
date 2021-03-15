---
title: Vytváření a aktualizace časových úseků pro vyzvednutí zákazníkem
description: V tomto tématu je popsán postup při vytváření, konfiguraci a aktualizaci časových úseků vyzvednutí zákazníkem v centrále Commerce.
author: anupamar-ms
manager: AnnBe
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: 125696e8f32c2452a572a2316f512779f399f5c4
ms.sourcegitcommit: 8b4cb7b6ad4aab37566bcc91e426bd56db771416
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/06/2021
ms.locfileid: "4828204"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a>Vytváření a aktualizace časových úseků pro vyzvednutí zákazníkem

[!include [banner](../../includes/banner.md)]

V tomto tématu je popsán postup při vytváření, konfiguraci a aktualizaci časových úseků vyzvednutí zákazníkem v centrále Commerce.

Funkce časového úseku poskytuje maloobchodníkům způsob, jak definovat časový úsek pro položky, pro které je zapnut způsob vyzvednutí/doručení zákazníkovi. Časové úseky umožňují maloobchodníkům definovat dny a časy, kdy lze objednávky vyzvednout v obchodě. Maloobchodníci mohou také definovat počet objednávek, které lze vyzvednout během daného období. Tímto způsobem mohou maloobchodníci omezit počet objednávek, které lze vyzvednout v daný den a v daný čas. Výsledkem je kvalitnější služba jejich zákazníkům.

> [!NOTE]
> Funkce časového úseku je k dispozici v Microsoft Dynamics 365 Commerce verze 10.0.15 a novější.

Následující obrázek ukazuje příklad výběru časového úseku na pokladně elektronického obchodu.

![Příklad výběru časového úseku v pokladně elektronického obchodu](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a>Vlastnosti časového úseku

Časový úsek je konkrétní interval, kdy si zákazník může zvolit vyzvednutí objednávky z konkrétního obchodu nebo místa. Funkce správy časových slotů je k dispozici pouze v případě, že je nakonfigurován způsob vyzvednutí/doručení zákazníkovi v Dynamics 365 Commerce.

Časový úsek je definován pomocí následujících vlastností:

- **Způsob doručení** – Zadejte způsob vyzvednutí dodávky, na které se vztahuje časový úsek.
- **Minimální počet dní** a **Maximální počet dní** – Zadejte nejdřívější a nejpozdější datum, které lze vybrat k vyzvednutí relativně k datu, kdy je objednávka podána. 

    Vlastnost **Minimální počet dní** zajišťuje, že maloobchodník má dostatek času na zpracování objednávky, než bude připravena k vyzvednutí. Vlastnost **Maximální počet dní** zajišťuje, že uživatel nemůže vybrat datum, které je příliš daleko v budoucnosti. Například pokud je minimální hodnota nastavena na **1** a objednávka je podána 20. září, nejdřívější den, kdy bude objednávka dostupná k vyzvednutí, je následující možný den (21. září). Podobným způsobem můžete nastavením maximální hodnoty definovat maximální počet dní, po které lze objednávku vyzvednout. Když jsou definovány minimální a maximální hodnoty, uživatelé webu mohou během procesu placení zobrazit a vybrat pouze konkrétní sadu dnů.

    Minimální hodnotu můžete nastavit na desetinnou hodnotu, která je menší než 1. Pokud je například vyzvednutí k dispozici čtyři hodiny po zadání objednávky, nastavte minimální hodnotu na **0,17** (= 4 ÷ 24, zaokrouhleno nahoru na dvě desetinná místa). Pokud však nastavíte minimální hodnotu na desetinnou hodnotu, která je větší než 1, vždy se zaokrouhlí nahoru na nejbližší celé číslo. Například hodnota **1,2** bude zaokrouhlena na **2**. Podobně, pokud nastavíte maximální hodnotu na desetinnou hodnotu, vždy se zaokrouhlí nahoru na nejbližší celé číslo. 

- **Počáteční datum** a **Koncové datum** – Zadejte počáteční a koncové datum časového úseku. Každá položka časového úseku má počáteční a koncové datum. Proto máte flexibilitu pro přidávání různých časových úseků po celý rok (například vyzvednutí během svátků). Pokud se po zadání objednávky změní počáteční a koncové datum časového úseku, změny se na danou objednávku nebudou vztahovat. Když definujete počáteční a koncové datum, musíte zvážit data uzavření obchodu (například Boží hod vánoční) a zajistit, aby pro tyto dny nebyly definovány časové úseky.
- **Aktivní hodiny vyzvednutí** – Zadejte období, kdy je vyzvednutí povoleno. Například časy vyzvednutí mohou být každý den mezi 14:00 a 17:00. Tato vlastnost umožňuje, aby časy vyzvednutí byly nezávislé na hodinách obchodu. Proto může maloobchodník nakonfigurovat časy vyzvednutí, které splňují jeho specifické obchodní požadavky. Když definujete aktivní hodiny vyzvednutí, musíte vzít v úvahu provozní hodiny obchodu a zajistit, aby časy vyzvednutí nebyly definovány pro časy, kdy je obchod zavřený.

    > [!NOTE]
    > Hodiny vyzvednutí v obchodě musí být definovány v časovém pásmu příslušného obchodu.

- **Interval časového úseku** – Zadejte dobu trvání jednotlivých časových úseků. Například doba trvání každého časového úseku může být v přírůstcích po 15 minutách, 30 minutách nebo jedné hodině. Pokud je hodnota časového úseku 0, je časový úsek k dispozici po celou dobu mezi počátečním a koncovým časem.
- **Úseky na interval** – Zadejte počet zákazníků nebo objednávek, které mohou být obslouženy k vyzvednutí během každého intervalu časového úseku. Například zadejte **1**, **2**, **3** nebo jakékoli jiné celé číslo.
- **Aktivní dny** – Zadejte dny v týdnu, kdy jsou aktivní časové úseky vyzvednutí. Tato vlastnost umožňuje maloobchodníkovi definovat dny, kdy chce podporovat vyzvednutí objednávek.
- **Maloobchodní kanály** – Zadejte maloobchodní kanály. Každý časový úsek může být přidružen k jednomu nebo více maloobchodním obchodům. V závislosti na provozních hodinách každého obchodu lze vytvořit jeden nebo více položek časových úseků a přidružit je ke kanálu. 

<!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

Pro každý kanál lze nakonfigurovat pouze jednu šablonu časového úseku. Tyto kanály zahrnují kamenné obchody, kontaktní střediska, mobilní zařízení a weby s elektronickým obchodováním.

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a>Konfigurace funkce časového úseku v centrále Commerce

Časové úseky musí být definovány pro každý způsob vyzvednutí v centrále Commerce, aby na ně mohly odkazovat pokladní místo (POS) a kanály elektronického obchodování.

- Ke každé šabloně časového úseku lze přidružit každý obchod nebo kanál.
- Každý vytvořený časový úsek by měl být jedinečný pro každý způsob doručení v každé šabloně.
- Po nakonfigurování funkce časového úseku bude kalendář časového úseku k dispozici vybraným obchodům nebo skupinám obchodů. Bude také viditelný v POS pro přehled.

Konfiguraci funkce časového úseku v centrále Commerce provedete následovně.

1. Jděte na **Commerce** \> **Nastavení kanálu** \> **Časový úsek vyzvednutí v obchodě**.
1. Zvolte **Nový** pro vytvoření nové šablony časového úseku. Chcete-li použít existující šablonu, vyberte ji v levém podokně.
1. Zadejte hodnoty do polí **ID časového úseku** a **Popis**.
1. Na záložce s náhledem **Vyzvednutí objednávky – nastavení času** vyberte **Přidat**.
1. V dialogovém okně **Vyzvednutí objednávky – nastavení času** definujte rozsah dat, způsob doručení, aktivní hodiny doručení, aktivní dny, interval časového úseku, úseky na interval a další nastavení.

    Pokud budou časové úseky v dohledné budoucnosti statické, nastavte pole **Koncové datum** na **Nikdy**.

    > [!NOTE]
    > Můžete vytvořit více šablon, ale k jednomu kanálu nebo obchodu lze přidružit pouze jednu šablonu.

    ![Dialogové okno Vyzvednutí objednávky – nastavení času](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. Po dokončení zvolte **OK**.
1. Pokud se časové úseky v některém dni budou lišit, vytvořte další položky na záložce s náhledem **Vyzvednutí objednávky – nastavení času**, abyste zajistili, že se data a časy nepřekrývají.
1. Na záložce s náhledem **Maloobchodní kanály** volbou **Přidat** přidružíte šablonu časového úseku k obchodům nebo kanálům, kde bude použita.
1. V dialogovém okně **Výběr uzlů organizace** pomocí šipek vyberte (nebo zrušte výběr) obchody, oblasti a organizace, ke kterým má být daná šablona přidružena.

    <!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. Po dokončení zvolte **OK**.
1. Na stránce **Plán distribuce** spusťte úlohu **1070** a **1135** pro synchronizaci dat s kanály.

## <a name="time-slot-selection-for-pos-orders"></a>Výběr časového úseku pro objednávky POS

Když je na POS identifikována objednávka nebo řádek objednávky pro vyzvednutí, může pokladník vybrat obchod nebo místo a datum a časový úsek pro vyzvednutí. Pokud má odběratel objednávku výdeje pro jiný obchod, může pokladník vybrat data, kdy bude výdej v daném obchodě k dispozici. Vyhledávání obchodu poskytne odkaz na data a pracovní doby obchodu.

Následující obrázek ukazuje příklad výběru časového úseku pro objednávku POS.

![Příklad výběru časového úseku pro objednávku POS](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a>Výběr časového úseku pro objednávky elektronického obchodu

Informace, jak zpřístupnit výběr časového úseku pro objednávky elektronického obchodu, viz [Modul informací o vyzvednutí](../pickup-info-module.md).

> [!NOTE]
> Uživatelé mohou prohlížet nebo upravovat časové úseky vyzvednutí na stránce pokladny na webu Commerce, pouze pokud byl na tuto stránku přidán modul s informacemi o vyzvednutí. Pokud stránka pokladny neobsahuje modul s informacemi o vyzvednutí, budou objednávky zadávány, aniž by uživatelé mohli zadávat nebo prohlížet informace o časových úsecích.

Následující obrázek ukazuje příklad objednávky elektronického obchodu, kde byl vybrán časový úsek vyzvednutí.

![Příklad objednávky elektronického obchodu, kde byl vybrán časový úsek vyzvednutí](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="time-slot-selection-for-call-center-orders"></a>Výběr časového úseku pro objednávky kontaktního střediska

V aplikaci kontaktního střediska mohou agenti kontaktního střediska vybrat obchod nebo umístění pro vyzvednutí, stejně jako datum a časový úsek, jak je zvýrazněno na následujícím obrázku.

![Příklad objednávky kontaktního střediska, kde byl vybrán časový úsek vyzvednutí](../dev-itpro/media/Curbside_timeslot_callcenter.png)

## <a name="additional-resources"></a>Další prostředky

[Modul informací o vyzvednutí](../pickup-info-module.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]