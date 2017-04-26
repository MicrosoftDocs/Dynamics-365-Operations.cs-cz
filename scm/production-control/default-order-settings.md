---
title: "Výchozí nastavení objednávky rozměry a varianty produktu"
description: "Výchozí nastavení objednávky definuje pracoviště a sklad, odkud pocházející nebo kde jsou uloženy položky, minimální, maximální, násobná a standardní množství, která budou použita pro obchodování nebo řízení skladu, doby realizace, příznaky pro zastavení a metody příslibu objednávek. Výchozí nastavení objednávek se používají při vytváření nákupních objednávek, prodejních objednávek, převodních příkazů, deníků zásob a na základě hlavního plánování pro generování plánovaných objednávek. Výchozích nastavení objednávek může být specifické podle položky, pracovišť, variant produktu nebo dimenze produktu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventItemOrderSetup
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223084
ms.assetid: fbfbcd7b-dc75-44ab-bffc-8bad576804a4
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 60abaa69debd891b2fe2dd98184c0dab50b0bf9f
ms.lasthandoff: 03/29/2017


---

# <a name="default-order-settings-for-dimensions-and-product-variants"></a>Výchozí nastavení objednávky rozměry a varianty produktu

[!include[banner](../includes/banner.md)]


Výchozí nastavení objednávky definuje pracoviště a sklad, odkud pocházející nebo kde jsou uloženy položky, minimální, maximální, násobná a standardní množství, která budou použita pro obchodování nebo řízení skladu, doby realizace, příznaky pro zastavení a metody příslibu objednávek. Výchozí nastavení objednávek se používají při vytváření nákupních objednávek, prodejních objednávek, převodních příkazů, deníků zásob a na základě hlavního plánování pro generování plánovaných objednávek. Výchozích nastavení objednávek může být specifické podle položky, pracovišť, variant produktu nebo dimenze produktu.

Výchozí nastavení objednávky můžete definovat na stránce **Výchozí nastavení objednávky**. Chcete-li tuto stránku otevřít, přejděte na **řízení informací o produktech**&gt;**produkty**&gt;**uvolněných produktů**&gt; vyberte uvolněný produkt &gt;na **plán** nebo *** Správa zásob *** v podokně akcí &gt;**nastavení pořadí**&gt;**výchozí nastavení objednávky**.

## <a name="default-order-settings"></a>Výchozí nastavení objednávky
Existují tři typy výchozího nastavení objednávky pro nákupy, prodeje a zásoby. Výchozí nastavení objednávky pro nákup se používá při vytváření:

-   Řádky nákupní objednávky
-   Řádky nákupní smlouvy
-   Řádky požadavku na nabídku
-   Řádky nákupní žádanky
-   Řádky doplnění stavu zásob dodávky
-   Plánované nákupní objednávky

Výchozí nastavení objednávky pro prodej se používá při vytváření:

-   Řádky prodejní objednávky
-   Řádky prodejní smlouvy
-   Řádky prodejní nabídky
-   Řádky vratky a řádky náhrady položky
-   Řádky prognózy poptávky

Výchozí nastavení objednávky pro prodej se dále používá při vytváření:

-   Požadavky položek projektu
-   Požadavků na položku servisní objednávky

Výchozí nastavení objednávky pro zásoby se používá při vytváření:

-   Skladové deníky
-   Převodní příkazy
-   Plánované převodní příkazy

Výchozí nastavení objednávky pro zásoby se dále používá při vytváření:

-   Karanténní příkazy
-   Objednávky kvality
-   Výrobní zakázky
-   Řádky kusovníku
-   Plánované výrobní zakázky

## <a name="full-definition-of-a-released-product"></a>Úplná definice uvolněného produktu
Při vytváření transakce, je třeba zadat úplnou definici uvolněný produkt na řádku před 365 Dynamics pro operace se pokusí zjistit výchozí nastavení objednávky. Úplná definice uvolněný produkt znamená, že číslo položky a všechny aktivní dimenze produktu, jako je například konfigurace, velikost, styl a barvu, jsou zadána v transakci. Pokud například ručně vytvoříte řádek nákupní objednávky pro variantu uvolněného produktu, je nutné zadat všechny dimenze požadovaného produktu předtím, než se pracoviště, sklad, množství a doba realizace zobrazí ve výchozím nastavení na řádku objednávky. 

Ne všechny parametry výchozí nastavení objednávky jsou použity při vytváření řádků objednávky nebo deníku. Množství a doba realizace se zobrazí ve výchozím nastavení v případě potřeby. Například pokud řádek deníku počítání, pracoviště a sklad se zobrazí ve výchozím nastavení při vytvoření řádku. Samozřejmě žádné výchozí množství nebo více kontroly a minimální jsou prováděny při vytvoření řádku nebo zaúčtování deníku. 

Systém se vždy pokouší najít výchozí pracoviště a sklad při vytvoření řádku objednávky nebo deníku. Pracoviště se nezobrazuje vždy defaultně z nastavení objednávky. Například při vytváření prodejní objednávky nebo nákupní objednávky se v řádcích objednávky automaticky použije pracoviště v záhlaví objednávky. Při vytváření řádku Kusovníku, web ze záhlaví Kusovníku používá. Poté, co je web určen, se použije k vyhledání libovolného webu nastavení objednávky specifické, které pak slouží jako výchozí pro sklad. 

Výchozí typ objednávky, nákup a doby realizace zásob lze přepsat pomocí pravidla disponibility položky na **Disponibilita položky** stránky. Přestože výchozí nastavení objednávky neumožňuje rozdíl mezi produkcí a doba realizace převodu, vezme se pravidla disponibility pro položku. Nastavení disponibility položky však použije jen MRP při vytváření objednávek plánované výroby a plánovaného převodu a nebude použito při ručním vytváření objednávek výroby a převodu. 

## <a name="default-order-settings-rules"></a>Pravidla výchozího nastavení objednávky
Můžete definovat obecné výchozí nastavení objednávky a libovolný počet pravidel výchozího nastavení, která se použijí pouze v určitých podmínkách, například v pracovišti nebo ve specifických dimenzích produktu nebo v kombinacích dimenzí produktu. Není možné definovat nastavení objednávky specifické pro sklad.

### <a name="rank-in-default-order-settings"></a>Kategorie výchozích nastavení objednávky

Pravidla výchozího nastavení objednávky mají kategorie. Čím vyšší kategorie, tím důležitější pravidlo je, což znamená, že má vyšší prioritu a používá se před pravidly nižší kategorie. Obecné výchozí nastavení objednávky má kategorii nula, což nelze změnit. Může existovat pouze jedno pravidlo záznam s kategorií 0. Pravidla mohou mít stejnou kategorii za předpokladu, že se dimenze mají lišit. To je užitečné pro nastavení objednávky s místními specifiky. Při vytváření nového pravidla výchozího nastavení objednávky mají hodnoty pro hodnoty objednávky, příznaky pro zastavení atd. kategorii nula, mohou ale být přepsány.

### <a name="default-order-settings-for-released-products"></a>Výchozí nastavení objednávky pro uvolněné produkty

Pro různé uvolněné produkty můžete definovat obecné nastavení objednávky nebo nastavení objednávky specifické pro pracoviště. Obecná nastavení objednávky budou mít vždy kategorii nula. Nastavujete-li nové prodejní, nákupní a skladové objednávky společně a současně, doporučujeme používat **Zobrazení podrobností** na stránce **Výchozí nastavení objednávky **. Chcete-li přepnout do zobrazení Podrobnosti, přejděte **možností** podokno akcí &gt;**stránky možnosti**&gt;**změnit zobrazení**&gt;**zobrazení podrobností**.

### <a name="site-specific-order-settings"></a>Nastavení objednávky specifické pro pracoviště

Pro vytvoření nastavení objednávky specifické pro pracoviště, klepněte na tlačítko **Nový**. V **zobrazení podrobností**, vyplňte na webu v **nastavení pro**&gt;**web** pole. V **Zobrazení mřížky** vyplňte pracoviště ve sloupci **Pracoviště**. Nové pravidlo získá automaticky novou hodnotu kategorie vyšší než nula. Můžete vytvořit tolik pravidel specifických podle pracovišť, kolik potřebujete a můžete přiřadit všechna specifická pravidla podle pracovišť, abyste vymodelovali, že jsou stejně důležitá. 

Pokud jste v **Zobrazení podrobností** nemůžete získat přehled pravidel, které jsou vytvořena pro položku. Přepněte tlačítkem **Zobrazit seznam** pro zobrazení informací o přehledu. Když je vytvořen řádek objednávky libovolného typu a nemá žádný web k dispozici, 365 Dynamics pro operace Vyhledá pravidlo s zadaný žádný web. To může pomoci určit výchozí web na řádku objednávky. Toto pracoviště se pak používá k vyhledávání pravidla specifického pro pracoviště, pokud může být nastaven výchozí sklad. Tento sklad je použit pro daný řádek objednávky.

### <a name="specific-order-settings-for-product-dimension"></a>Specifické nastavení objednávky pro dimenzi produktu

Můžete definovat pravidla nastavení objednávek pro všechny aktivní dimenzi produktu nebo aktivní kombinaci dimenzí produktu. Jestliže je pole dimenze produktu prázdné, bude se pravidlo vztahovat na všechny hodnoty dimenze produktu. 

Představte si následující vzorový produkt:

|                                                     |                                         |
|-----------------------------------------------------|-----------------------------------------|
| **Product name**                                    | Fotoelektrický snímač                    |
| **Item number**                                     | XW56                                    |
| **Konfigurace** (používá se k modelaci typu osvětlení) | C1 - viditelné červené světlo, C2 - infračervené světlo |
| **Styl** (slouží k modelování strojní revize)  | R1, R2, R3                              |

V tomto příkladu předpokládejme, že produkt je pořízeny a ne vyrobený. Také předpokládejme, že konfigurace C1 se běžně používá, takže má kratší dobu realizace. 

Vytvořte následující výchozí nastavení objednávky k modelování této situace.

| Rozsah | Pracoviště | Konfigurace | Styl | Nákup - Přepsat výchozí nastavení | Doba realizace nákupu | Zastavený nákup | Prodej - Přepsat výchozí nastavení | Prodeje – zastaveno |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C1            |       | Ano                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Při vytváření řádku nákupní objednávky nebo plánované nákupní objednávky pro XW56, konfigurace C1 bez ohledu na revize nebo pracoviště, k němuž se přiřazuje řádek, bude doba realizace 2. Předpokládejme, že budou zastaveny všechny revize kromě R3.

Můžete vytvořit následující výchozí pravidla nastavení objednávky.

| Rozsah | Pracoviště | Konfigurace | Styl | Nákup - Přepsat výchozí nastavení | Doba realizace nákupu | Zastavený nákup | Prodej - Přepsat výchozí nastavení | Prodeje – zastaveno |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 20   |      |               | R2    | Ano                                  |                    | Ano                | Ano                               | Ano             |
| 20   |      |               | R1    | Ano                                  |                    | Ano                | Ano                               | Ano             |
| 10   |      | C1            |       | Ano                                  | 2                  |                    |                                   |                 |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Obě pravidla pro ukončení starých revizí mají stejnou kategorii, což znamená, že jsou stejně důležitá. Obě mají vyšší kategorii než pravidla konfigurace C1, což znamená, že mají přednost před pravidly konfigurace C1. 

Tento příklad vysvětluje potřebu kategorií. Když vzniká nákupní objednávka pro konfiguraci C1 a revizi R2, bez kategorií, budou obě pravidla pro R2 a C1 nejednoznačná. Pro vyřešení nejednoznačnosti bude Dynamics 365 for Operations hledat pravidla v sestupném pořadí kategorií a použije první vhodné pravidlo. V tomto příkladu, když se tvoří řádku nákupní objednávky pro konfiguraci C1 a revizi R2, získá uživatel zprávu s upozorněním, že položka je blokována a že je to způsobeno hodnotou revize. Pokud má pravidlo pro konfiguraci a vyšší kategorii než pro revize, potom bude následovat vytvoření řádku nákupní objednávky pro konfiguraci C1 a revizi R2 a žádná zpráva o 'blokování položky' nebude uživateli odeslána. 

Zvažte následující výchozí pravidla nastavení objednávky.

| Rozsah | Pracoviště | Konfigurace | Styl | Výchozí pracoviště | Výchozí sklad | Nákup - Přepsat výchozí dimenze úložiště | Nákupní sklad |
|------|------|---------------|-------|--------------|-------------------|------------------------------------------------|--------------------|
| 20   | 2    |               |       |              |                   | Ano                                            | 22                 |
| 10   |      | C1            |  R2   |  2           |  21               |                                                |                    |
| 0    |      |               |       | 1            | 11                |                                                |                    |

Systém překročí sady pravidel dvakrát za účelem stanovení pracovišť a skladů. Při vytvoření řádku nákupní objednávky pro konfiguraci C1, R2, styl webu závisí na pravidlo s pořadím 10. Potom systém vyhledá pravidlo pro web 2 pro stanovení skladu. Je nalezeno pravidlo 20 a vzhledem k tomu, že má vyšší kategorii, sklad na řádku nákupní objednávky bude 22 a ne 21. 

Jako hlavní pokyny slouží specifická pravidla a pravidla pro dimenze, které jsou důležitější než jiné dimenze, získávají vyšší kategorie, zatímco obecnější pravidla získávají nižší kategorie. 

Pravidlo s kategorií nula slouží jako záchranná síť. Jestliže nedojde k aplikaci žádných dalších pravidel, pak se použije výchozí nastavení objednávky od pravidla nula. 

Vzhledem k tomu, že je kategorie tak důležitá, jsou v podokně akcí **výchozí nastavení objednávky ** funkce pro přesun pravidla nahoru nebo dolů a pro přečíslování, takže jsou vždy s nárůstem 10. 

Pravidel vytvořených pro uvolněný produkt může být více. Chcete-li získat lepší představu o tom, co každé pravidlo přepisuje a proč je to zapotřebí, doporučujeme používat **zobrazení mřížky** na stránce** výchozí nastavení objednávky**. Zobrazení mřížky můžete povolit tak, že přejdete k **možností** podokno akcí &gt;**stránky možnosti**&gt;**změnit zobrazení**&gt;**zobrazení mřížky**. Počet zobrazených sloupců v mřížce může být celkem významný, zejména pro karty prodeje a zásob. Chcete-li omezit počet sloupců v mřížce zobrazeny, skupiny sloupců skryty nebo zobrazeny pomocí tlačítek na **výchozí nastavení objednávky**&gt;**zobrazení sloupců** nabídky.

### <a name="specific-order-settings-for-released-product-variant"></a>Specifické nastavení objednávky pro variantu uvolněného produktu

Pokud systém pravidel pro výchozí nastavení objednávky je příliš těžkopádný, je možné jednoduše definovat výchozí nastavení objednávek pro každou variantu produktu. Následující příklady ukazují, jak to vypadá pro produkt a výše popsané případy.

| Rozsah | Pracoviště | Konfigurace | Styl | Nákup - Přepsat výchozí nastavení | Doba realizace nákupu | Zastavený nákup | Prodej - Přepsat výchozí nastavení | Prodeje – zastaveno |
|------|------|---------------|-------|--------------------------------------|--------------------|--------------------|-----------------------------------|-----------------|
| 10   |      | C2            | R3    | Ano                                  | 5                  |                    |                                   |                 |
| 10   |      | C2            | R2    | Ano                                  | 5                  | Ano                | Ano                               | Ano             |
| 10   |      | C2            | R1    | Ano                                  | 5                  | Ano                | Ano                               | Ano             |
| 10   |      | C1            | R3    | Ano                                  | 2                  |                    |                                   |                 |
| 10   |      | C1            | R2    | Ano                                  | 2                  | Ano                | Ano                               | Ano             |
| 10   |      | C1            | R1    | Ano                                  | 2                  | Ano                | Ano                               | Ano             |
| 0    |      |               |       |                                      | 5                  |                    |                                   |                 |

Na kategorii v tomto případě příliš nezáleží, proto ji můžete zakrýt. Toto řešení může uvádět problém s údržbou. Můžete však zvážit použití tohoto nastavení, pokud berete v úvahu integraci systémů správy životního cyklu produktu (PLM).




