---
title: Podrobnosti řádku práce
description: Toto téma uvádí informace o stránce Podrobnosti řádku práce, která zobrazuje kompletní, řaditelný a filtrovatelný seznam jednotlivých řádků práce v systému.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkLocationChange, WHSWorkLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: bcb340b21e06b294a40784bf3a1da71b0daf7655
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015888"
---
# <a name="work-line-details"></a>Podrobnosti řádku práce

[!include [banner](../includes/banner.md)]

Stránka **Podrobnosti řádku práce** zobrazuje kompletní, řaditelný a filtrovatelný seznam jednotlivých řádků práce v systému. Umožňuje zobrazit úplný přehled prací, které jsou ve skladu plánovány a realizovány. Mezi zobrazením všech řádků práce a zobrazením pouze otevřených řádků práce můžete snadno přepínat. Podrobnosti poskytované pro každý řádek práce zahrnují stav práce, číslo položky, skladové místo, pracovní množství, ID nákladu a ID dodávky.

## <a name="turn-on-the-work-line-details-feature"></a>Zapnutí funkce podrobností řádku práce

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, je-li to potřeba. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Řízení skladu*
- **Název funkce:** *Podrobností řádku práce*

## <a name="open-and-use-the-work-line-details-page"></a>Otevření a použití stránky Podrobnosti řádku práce

Chcete-li zobrazit seznam podrobností řádku práce, přejděte na **Řízení skladu \> Práce \> Podrobnosti řádku práce**. Odtud můžete provést následující akce:

- Pole **Filtr** umožňuje hledat řádky, jež obsahují konkrétní hodnotu některého z dostupných parametrů. (Dostupné parametry zahrnují mnoho parametrů, jež nejsou zobrazeny, například sloupce v mřížce.)
- Přepínám pomocí zaškrtávacího políčka **Zobrazit uzavřené** můžete zobrazit nebo skrýt uzavřené řádky.
- Volbou **Zobrazit dimenze** můžete otevřít dialogové okno **Zobrazení dimenzí** , kde můžete vybrat, zda chcete zobrazit nebo skrýt sloupce různých dimenzí v mřížce.
- Výběrem libovolného záhlaví sloupce otevřete nabídku, kde si můžete vybrat třídění nebo filtrování seznamu podle hodnot v příslušném sloupci.
- Vyberte řádek práce a poté položku **Změnit skladové místo**. Otevře se dialogové okno, v němž můžete změnit skladové místo tohoto řádku práce. Skladové místo, které určíte, přepíše nastavení podle směrnice skladového místa.
- Vyberte řádek práce a poté možnost **Zrušit řádek práce**. Otevře se dialogové okno, v němž můžete částečně nebo úplně zredukovat množství v daném řádku práce.
- Úpravy množství.
- Zobrazení transakcí spojených s řádkem práce.

## <a name="try-out-the-feature"></a>Vyzkoušejte tuto funkci

Tato část obsahuje ukázku složenou ze tří částí, jež demonstruje, jak pracovat s podrobnostmi řádku práce.

### <a name="make-sample-data-available"></a>Příprava ukázkových dat

Chcete-li s touto ukázkou pracovat pomocí zde specifikovaných ukázkových záznamů a hodnot, musíte používat systém, ve kterém jsou nainstalována standardní [ukázková data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md). Kromě toho musíte dříve, než začnete, také vybrat právnickou osobu **USMF**.

Tuto ukázku můžete také použít jako vodítko při práci na produkčním systému. Musíte však nahradit uvedené hodnoty vlastními hodnotami. Také možná budete postrádat některé typy požadovaných záznamů, jež jsou součástí standardních ukázkových dat.

### <a name="verify-that-the-scenario-setup-includes-enough-available-inventory"></a>Ověření, že nastavení scénáře obsahuje dostatečné dostupné zásoby

Pokud pracujete s ukázkovými daty **USMF** , měli byste se nejprve ujistit, že je váš systém nastaven tak, aby na každém relevantním skladovém místě pro výdej byly k dispozici dostatečné zásoby. V rámci této ukázky se očekává, že budete mít k dispozici následující zásoby:

- **Položka M9200:** 45 ks (nebo více)
- **Položka M9202:** 10 ks (nebo více)

Chcete-li ověřit, že máte k dispozici dostatečné zásoby, případně provést potřebné úpravy, poustupujte podle těchto kroků.

1. Přejděte do **Řízení skladu \> Nastavení \> Směrnice skladového místa** a určete, která výdejová skladová místa se používají pro výdej prodejních objednávek ve skladu 51. (Další informace naleznete v tématu [Řízení práce ve skladu pomocí šablon práce a směrnic skladového místa](control-warehouse-location-directives.md).)
1. Zkontrolujte úrovně zásob na příslušných skladových místech.
1. Dle potřeby zásoby upravte. K úpravě úrovně zásob můžete vytvořit ruční pohyby, použít doplnění nebo jakýkoli jiný tok.

### <a name="part-1-create-picking-work"></a>Část 1: Vytvoření práce výdeje

Než začnete vytvářet práci, ujistěte se, že máte sklad nastaven tak, aby na požadavky na práci reagoval očekávaným způsobem.

Při vytváření práce výdeje postupujte takto:

1. Přejděte na **Prodej a marketing \> Prodejní objednávky \> Všechny prodejní objednávky**.
1. Kliknutím na možnost **Nová** otevřete dialogové okno **Vytvoření prodejní objednávky**.
1. V dialogovém okně **Vytvoření prodejní objednávky** nastavte následující hodnoty:

    - Na záložce s náhledem **Odběratel** zadejte do pole **Účet odběratele** hodnotu _US-001_.
    - Na záložce s náhledem **Obecné** zadejte do pole **Sklad** hodnotu _51_.

1. Vyberte **OK** , prodejní objednávka se vytvoří a dialogové okno se zavře.
1. Otevře se nová prodejní objednávka. Obsahuje nový prázdný řádek v mřížce **Řádky prodejních objednávek**. Na tomto řádku nastavte následující hodnoty:

    - **Číslo položky:** _M9200_
    - **Množství:** _20_
    - **Jednotka:** _EA_

1. Vyberte nový řádek objednávky a poté v nabídce **Zásoby** vyberte možnost **Rezervace**. Otevře se stránka **Rezervace**.
1. Na stránce **Rezervace** klikněte na **Rezervovat šarži**. Ve skladu se provede rezervace celého množství vybraného řádku.
1. Zavřete stránku **Rezervace** a vraťte se k prodejní objednávce.
1. V podokně Akce na kartě **Sklad** vyberte možnost **Uvolnit do skladu**. Systém vytvoří dodávku, přidá ji k novému nákladu a vytvoří požadovanou práci.
1. Vytvořte druhou prodejní objednávku pro stejný účet odběratele a sklad, jaké jste použili pro první objednávku. K této objednávce přidejte následující dva řádky objednávky:

    - **Řádek 1:** Nastavte v poli **Číslo položky** hodnotu _M9200_ , v poli **Množství** hodnotu _25_ a v poli **Jednotka** hodnotu _ks_.
    - **Řádek 2:** Nastavte v poli **Číslo položky** hodnotu _M9202_ , v poli **Množství** hodnotu _10_ a v poli **Jednotka** hodnotu _ks_.

1. Zopakujte kroky 6 až 8 a rezervujte zásoby pro každý řádek objednávky (vždy po jednom). Poté zopakujte krok 9 a uvolněte objednávku do skladu.

### <a name="part-2-change-the-location-for-a-work-line"></a>Část 2: Změna skladového místa pro řádek práce

1. Přejděte do nabídky **Řízení skladu \> Práce \> Podrobnosti řádku práce**.
1. Najděte a vyberte jeden řádek práce, který jste v rámci této ukázky vytvořili.
1. Vyberte možnost **Změnit skladové místo**. Otevře se dialogové okno **Výběr nového skladového místa**.
1. V dialogovém okně **Výběr nového skladového místa** vyberte v poli **Skladové místo** nové skladové místo pro řádek práce.
1. Vyberte **OK** , pokud chcete změnu použít. Dialogové okno se zavře.

> [!IMPORTANT]
> Změnu skladového místa můžete zadat, pouze když je na novém skladovém místě k dispozici dostatek zásob (pro výdej) nebo pokud skladové místo předává ověření typu skladového místa (pro vložení).

### <a name="part-3-change-the-quantity-of-a-work-line-or-cancel-a-work-line"></a>Část 3: Změna množství na řádku práce nebo zrušení řádku práce

1. Přejděte do nabídky **Řízení skladu \> Práce \> Podrobnosti řádku práce**.
1. Najděte a vyberte jeden řádek práce, který jste v rámci této ukázky vytvořili. Množství můžete zrušit nebo změnit pouze pro řádky práce, kde je typ práce _Výdej_.
1. Vyberte možnost **Zrušit řádek práce** , otevře se dialogové okno **Množství ke zrušení**.
1. V dialogovém okně **Množství ke zrušení** zadejte do pole **Množství** hodnotu odpovídající množství, jež se má *odečíst od* množství, jež je na řádku aktuálně zadáno. Ve výchozím nastavení se v poli **Množství** zobrazuje plné množství.

    - Pokud zrušíte celé množství, změní se hodnota položky **Stav práce** na _Zrušeno_. V poli **Množství práce** se ale bude stále zobrazovat původní hodnota.
    - Pokud zrušíte pouze část množství, hodnota v poli **Množství práce** se změní a bude zobrazovat novou hodnotu, Hodnota **Stav práce** se nezmění.

1. Vyberte **OK** , pokud chcete změnu použít. Dialogové okno se zavře.

> [!IMPORTANT]
> Pokud zrušíte jen část množství řádku práce, musíte také odstranit již neplatné množství z řádku nákladu. V opačném případě, pokud nebude dodávka nastavena správně, nebude možné potvrdit řádek nákladu k odeslání.
