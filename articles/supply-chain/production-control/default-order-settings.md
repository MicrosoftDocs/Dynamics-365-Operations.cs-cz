---
title: Výchozí nastavení objednávky pro dimenze a varianty produktů
description: Výchozí nastavení objednávky definuje pracoviště a sklad, odkud pocházející nebo kde jsou uloženy položky, minimální, maximální, násobná a standardní množství, která budou použita pro obchodování nebo řízení skladu, doby realizace, příznaky pro zastavení a metody příslibu objednávek.
author: t-benebo
manager: tfehr
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemOrderSetup, InventItemIdLookupByDefaultOrderSetting, EcoResProductReleasedStoppedAllChartPart, UnitTestPartitions
audience: Application User
ms.reviewer: kamaybac
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 2202b6b50d4b4b675759275379023a182b01af17
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007259"
---
# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Výchozí nastavení objednávky pro dimenze a varianty produktu

[!include [banner](../includes/banner.md)]

Výchozí nastavení objednávky v Dynamics 365 Supply Chain Management definuje pracoviště a sklad, odkud pocházející nebo kde jsou uloženy položky, minimální, maximální, násobná a standardní množství, která budou použita pro obchodování nebo řízení skladu, doby realizace, příznaky pro zastavení a metody příslibu objednávek. Výchozí nastavení objednávek se používají při vytváření nákupních objednávek, prodejních objednávek, převodních příkazů, deníků zásob a na základě hlavního plánování pro generování plánovaných objednávek. Výchozích nastavení objednávek může být specifické podle položky, pracovišť, variant produktu nebo dimenze produktu.

Chcete-li definovat výchozí nastavení objednávky pro produkt, postupujte takto.

1. Přejděte na **Řízení informací o produktech** &gt; **Produkty** &gt; **Uvolněné produkty**.
1. Vyberte relevantní produkt v mřížce.
1. Na podokně akcí otevřete soubor pomocí jednoho z těchto kroků stránku **Výchozí nastavení objednávky** pro vybraný produkt:

    - Na **Plán** kartě, ve skupině **Nastavení objednávky**, vyberte **Výchozí nastavení objednávky**.
    - Na **Spravovat sklad** kartě, ve skupině **Nastavení objednávky**, vyberte **Výchozí nastavení objednávky**.

1. Nakonfigurujte nastavení podle popisu ve zbytku tohoto tématu.

## <a name="default-order-settings"></a>Výchozí nastavení objednávky

Existují tři typy výchozího nastavení objednávky pro nákupy, prodeje a zásoby. Výchozí nastavení objednávky pro nákup se používá při vytváření:

- Řádky nákupní objednávky
- Řádky nákupní smlouvy
- Řádky požadavku na nabídku
- Řádky nákupní žádanky
- Řádky doplnění stavu zásob dodávky (částečně podporováno, viz poznámka)
- Plánované nákupní objednávky

> [!NOTE]
> U řádků objednávky doplnění stavu zásob dodávky je jediným nastavením z pevné záložky **Nákupní objednávka** na stránce **Výchozí nastavení objednávky**, které platí, pole **Výchozí web**, **Výchozí sklad** a zaškrtávací políčko **Zastaveno**.

Výchozí nastavení objednávky pro prodej se používá při vytváření:

- Řádky prodejní objednávky
- Řádky prodejní smlouvy
- Řádky prodejní nabídky
- Řádky vratky a řádky náhrady položky
- Řádky prognózy poptávky

Výchozí nastavení objednávky pro prodej se dále používá při vytváření:

- Požadavky položek projektu
- Požadavků na položku servisní objednávky

Výchozí nastavení objednávky pro zásoby se používá při vytváření:

- Skladové deníky
- Převodní příkazy
- Plánované převodní příkazy

Výchozí nastavení objednávky pro zásoby se dále používá při vytváření:

- Karanténní příkazy
- Objednávky kvality
- Výrobní zakázky
- Řádky kusovníku
- Plánované výrobní zakázky

## <a name="full-definition-of-a-released-product"></a>Úplná definice uvolněného produktu

Při vytváření transakce je třeba zadat úplnou definici uvolněného produktu na řádku, aby se aplikace Supply Chain Management pokusila zjistit výchozí nastavení objednávky. Úplné definování uvolněného produktu znamená, že se číslo položky a všechny aktivní dimenze produktu, například konfigurace, velikost, styl, verze a barva zadají v transakci. Pokud například ručně vytvoříte řádek nákupní objednávky pro variantu uvolněného produktu, je nutné zadat všechny dimenze požadovaného produktu předtím, než se pracoviště, sklad, množství a doba realizace zobrazí ve výchozím nastavení na řádku objednávky. 

Ne všechny parametry výchozí nastavení objednávky jsou použity při vytváření řádků objednávky nebo deníku. Ve výchozím nastavení budou zobrazeny pouze množství a doby realizace v případě potřeby. Například při výpočtu řádky deníku se zobrazí ve výchozím nastavení při vytvoření řádku pouze pracoviště a sklad. Z tohoto důvodu neprobíhají žádná výchozí nastavení množství nebo kontroly na násobcích a minimech při vytváření řádku nebo účtování deníku. 

Systém se vždy pokouší najít výchozí pracoviště a sklad při vytvoření řádku objednávky nebo deníku. Pracoviště se nezobrazuje vždy defaultně z nastavení objednávky. Například při vytváření prodejní objednávky nebo nákupní objednávky se v řádcích objednávky automaticky použije pracoviště v záhlaví objednávky. Vytváříte-li řádek kusovníku, je použito pracoviště v záhlaví kusovníku. Po určení pracoviště se toto použije k nalezení nastavení objednávky specifického pro pracoviště, které lze použít jako výchozí nastavení skladu. 

Výchozí typ objednávky, nákup a doba realizace skladu mohou být přepsány podle pravidla disponibility položky na stránce **Disponibilita položky**. Ačkoli výchozí nastavení objednávek neumožňuje rozlišovat mezi dobou realizace výroby a převodu, umožňují to pravidla disponibility položky. Nastavení disponibility položky však použije jen Master planning (MRP) při vytváření objednávek plánované výroby a plánovaného převodu a nebude použito při ručním vytváření objednávek výroby a převodu. 

## <a name="default-order-settings-rules"></a>Pravidla výchozího nastavení objednávky

Můžete definovat obecné výchozí nastavení objednávky a libovolný počet pravidel výchozího nastavení, která se použijí pouze v určitých podmínkách, například v pracovišti nebo ve specifických dimenzích produktu nebo v kombinacích dimenzí produktu. Není možné definovat nastavení objednávky specifické pro sklad.

### <a name="rank-in-default-order-settings"></a>Kategorie výchozích nastavení objednávky

Pravidla výchozího nastavení objednávky mají kategorie. Čím vyšší kategorie, tím důležitější pravidlo je, což znamená, že má vyšší prioritu a používá se před pravidly nižší kategorie. Obecné výchozí nastavení objednávky má kategorii nula, což nelze změnit. Může existovat pouze jedno pravidlo záznam s kategorií 0. Pravidla mohou mít stejnou kategorii za předpokladu, že se dimenze mají lišit. To je užitečné pro nastavení objednávky s místními specifiky. Při vytváření nového pravidla výchozího nastavení objednávky mají hodnoty pro hodnoty objednávky, příznaky pro zastavení atd. kategorii nula, mohou ale být přepsány.

### <a name="default-order-settings-for-released-products"></a>Výchozí nastavení objednávky pro uvolněné produkty

Pro různé uvolněné produkty můžete definovat obecné nastavení objednávky nebo nastavení objednávky specifické pro pracoviště. Obecná nastavení objednávky budou mít vždy kategorii nula. Nastavujete-li nové prodejní, nákupní a skladové objednávky současně, doporučujeme používat **Zobrazení podrobností** na stránce **Výchozí nastavení objednávky**. Pokud chcete přepnout na zobrazení podrobností, přejděte na **Možnosti**&gt; **Možnosti stránky** &gt; **Změnit zobrazení** &gt; **Zobrazení podrobností**.

### <a name="site-specific-order-settings"></a>Nastavení příkazu specifického pro pracoviště.

Pro vytvoření nastavení objednávky specifické pro pracoviště vyberte **Nový**. V **Zobrazení podrobností** vyplňte pracoviště do pole **Pracoviště** v sekci **Nastavení je použitelné pro**. V **Zobrazení mřížky** vyplňte pracoviště ve sloupci **Pracoviště**. Nové pravidlo je automaticky přiřazeno nové hodnotě kategorie, která je větší než 0 (nula). Můžete vytvořit tolik pravidel specifických podle pracovišť, kolik potřebujete. Chcete-li označit, že jsou stejně důležité, můžete všem pravidlům pro konkrétní web přiřadit stejnou hodnotu kategorie.

Pokud jste v **Zobrazení podrobností** nemůžete získat přehled pravidel, které jsou vytvořena pro položku. Použijte tlačítko **Zobrazit seznam** pro zobrazení informací o přehledu. Při vytváření řádku objednávky libovolného typu, pokud nemá zadané žádné pracoviště, hledá Supply Chain Management pravidlo bez určeného pracoviště. To pomůže určit výchozí pracoviště na řádku objednávky. Toto pracoviště se pak používá k vyhledávání pravidla specifického pro pracoviště, pokud může být nastaven výchozí sklad. Tento sklad je použit pro daný řádek objednávky.

### <a name="specific-order-settings-for-product-dimension"></a>Specifické nastavení objednávky pro dimenzi produktu

Můžete definovat pravidla nastavení objednávek pro všechny aktivní dimenzi produktu nebo aktivní kombinaci dimenzí produktu. Jestliže je pole dimenze produktu prázdné, bude se pravidlo vztahovat na všechny hodnoty dimenze produktu. 

Představte si následující vzorový produkt:

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Název produktu**                                    | Fotoelektrický snímač                    |
| **Číslo položky**                                     | XW56                                    |
| **Konfigurace** (používá se k modelaci typu osvětlení) | C1 - viditelné červené světlo, C2 - infračervené světlo |
| **Verze** | V1, V2, V3                              |

V tomto příkladu předpokládejme, že produkt je pořízeny a ne vyrobený. Také předpokládejme, že konfigurace C1 se běžně používá, takže má kratší dobu realizace. 

Vytvořte následující výchozí nastavení objednávky k modelování této situace.

| Rozsah | Lokalita | Konfigurace | Verze | Nákup - Přepsat výchozí nastavení | Doba realizace nákupu | Zastavený nákup | Prodej - Přepsat výchozí nastavení | Prodeje – zastaveno |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Ano                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Při vytváření řádku nákupní objednávky nebo plánované nákupní objednávky pro zboží XW56, konfigurace C1 bez ohledu na verzi nebo pracoviště, k němuž se přiřazuje řádek, bude doba realizace 2. Předpokládejme, že budou zastaveny všechny verze kromě V3.

Můžete vytvořit následující výchozí pravidla nastavení objednávky.

| Rozsah | Lokalita | Konfigurace | Verze | Nákup - Přepsat výchozí nastavení | Doba realizace nákupu | Zastavený nákup | Prodej - Přepsat výchozí nastavení | Prodeje – zastaveno |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | V2    | Ano                                  |                    | Ano                | Ano                               | Ano             |
| 20   |      |               | V1    | Ano                                  |                    | Ano                | Ano                               | Ano             |
| 10   |      | C1            |       | Ano                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Dvě pravidla pro zastavení starých verzí mají stejné pořadí. Proto jsou stejně důležité. Protože obě mají vyšší kategorii než pravidla konfigurace C1, mají přednost před pravidly konfigurace C1. 

Tento příklad vysvětluje potřebu kategorií. Když hodnota není použitá při vzniku nákupní objednávky pro konfiguraci C1 a verzi V2, bez kategorií, budou obě pravidla pro V2 a C1 nejednoznačná. Pro vyřešení nejednoznačnosti bude Supply Chain Management hledat pravidla v sestupném pořadí kategorií a použije první vhodné pravidlo. V tomto příkladu, když se tvoří řádku nákupní objednávky pro konfiguraci C1 a verzi V2, získá uživatel zprávu s upozorněním, že položka je blokována a že je to způsobeno hodnotou verze. Pokud má pravidlo pro konfiguraci a vyšší kategorii než pro verzi, potom bude následovat vytvoření řádku nákupní objednávky pro konfiguraci C1 a verzi V2 a žádná zpráva o 'blokování položky' nebude uživateli odeslána. 

Zvažte následující výchozí pravidla nastavení objednávky.

| Rozsah | Lokalita | Konfigurace | Verze | Výchozí pracoviště | Výchozí sklad | Nákup - Přepsat výchozí dimenze úložiště | Nákupní sklad |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Ano                                            | 22                 |
| 10   |      | C1            |  V2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Systém překročí sady pravidel dvakrát za účelem stanovení pracovišť a skladů. Při vytvoření řádku nákupní objednávky pro konfiguraci C1, verzi V2, je určeno pracoviště na základě pravidla s hodnotou 10. Poté systém hledá pravidlo pro pracoviště 2 s cílem určit sklad. Je nalezeno pravidlo 20 a vzhledem k tomu, že má vyšší kategorii, sklad na řádku nákupní objednávky bude 22, ne 21.

Jako hlavní pokyny slouží specifická pravidla a pravidla pro dimenze, které jsou důležitější než jiné dimenze, získávají vyšší kategorie, zatímco obecnější pravidla získávají nižší kategorie. 

Pravidlo s kategorií nula slouží jako záchranná síť. Jestliže nedojde k aplikaci žádných dalších pravidel, pak se použije výchozí nastavení objednávky od pravidla nula. 

Vzhledem k tomu, že je kategorie důležitá, jsou v podokně akcí **výchozí nastavení objednávky** funkce pro přesun pravidla nahoru nebo dolů a pro přečíslování, takže jsou vždy s nárůstem 10. 

Pravidel vytvořených pro uvolněný produkt může být více. Chcete-li získat lepší porozumění tomu, co každé pravidlo přepisuje a proč je to zapotřebí, doporučujeme používat **zobrazení mřížky** na stránce **výchozí nastavení objednávky**. Zobrazení mřížky lze povolit v **Možnosti**&gt; **Možnosti stránky** &gt; **Změnit zobrazení** &gt; **Zobrazení mřížky**. Počet zobrazených sloupců v mřížce může být celkem významný, zejména pro karty prodeje a zásob. Chcete-li omezit počet zobrazovaných sloupců v mřížce, můžete skrýt nebo zobrazit skupiny sloupců pomocí tlačítek v nabídce **Výchozí nastavení objednávky** &gt; **Zobrazení sloupce**.

### <a name="specific-order-settings-for-released-product-variant"></a>Specifické nastavení objednávky pro variantu uvolněného produktu

Pokud systém pravidel pro výchozí nastavení objednávky je příliš těžkopádný, je možné definovat výchozí nastavení objednávek pro každou variantu produktu. Následující příklad ukazuje, jak to vypadá pro produkt a výše popsané případy.

| Rozsah | Lokalita | Konfigurace | Verze | Nákup - Přepsat výchozí nastavení | Doba realizace nákupu | Zastavený nákup | Prodej - Přepsat výchozí nastavení | Prodeje – zastaveno |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | V3    | Ano                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | V2    | Ano                                  | 5                  | Ano                | Ano                               | Ano             |
| 10   |      | C2            | V1    | Ano                                  | 5                  | Ano                | Ano                               | Ano             |
| 10   |      | C1            | V3    | Ano                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | V2    | Ano                                  | 2                  | Ano                | Ano                               | Ano             |
| 10   |      | C1            | V1    | Ano                                  | 2                  | Ano                | Ano                               | Ano             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Na kategorii v tomto případě příliš nezáleží, proto ji můžete zakrýt. Toto řešení může uvádět problém s údržbou. Můžete však zvážit použití tohoto nastavení, pokud berete v úvahu integraci systémů správy životního cyklu produktu (PLM).

## <a name="use-strict-or-standard-validation-of-default-order-quantities"></a>Použijte přísné nebo standardní ověření výchozích množství objednávek

Můžete si vybrat, jak přísný by měl být systém při ověřování množství zadaného do **Výchozí nastavení objednávky** pro produkt. Když použijete novou přísnou možnost, **Množství standardní objednávky** musí být vždy násobkem zadané hodnoty **Násobek** nákupních objednávek, zásob a prodejních objednávek. Pokud používáte přísnou validaci, nebudete moci uložit výchozí nastavení objednávek, která nesplňují tento požadavek (a na liště zpráv se zobrazí chyba). 

Platí přísná validace na hodnoty **Množství standardní objednávky** uvedené na pevných záložkách **Nákupní objednávka**, **Zásoby** a **Prodejní objednávka** na stránce **Výchozí nastavení objednávky**. Každá pevná záložka má své vlastní nastavení **Násobek**, které se používá k ověření hodnoty **Množství standardní objednávky** zadané pro tuto pevnou záložku.

### <a name="enable-the-strict-validation-option"></a>Povolte možnost přísného ověření

Než můžete použít možnost přísné validace, musíte ji zapnout ve svém systému. Správci mohou pomocí stránky [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a povolit je v případě potřeby. Tato funkce je uvedena jako:

- **Modul** - *Řízení informací o produktech*
- **Název funkce** - *Přísná validace na výchozí množství objednávek*

### <a name="set-the-validation-option"></a>Nastavte možnost ověření

Nastavte možnost ověření takto:

1. Přejděte do **Správa informací o produktu \> Nastavení \> Parametry správy informací o produktu**.
1. Na kartě **Všeobecné** nastavte **Ověření výchozího množství objednávky** na jednu z následujících hodnot:
    - **Přísný** - Tuto možnost vyberte, chcete-li zajistit, aby všechny hodnoty **Množství standardní objednávky** byly násobkem hodnoty **Násobek** pro každou pevnou záložku (**Nákupní objednávka**, **Zásoby** a **Prodejní objednávka**).
    - **Standardní** - Tuto možnost vyberte, chcete-li použít standardní ověření (které funguje stejně, jako když tato funkce není povolena).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]