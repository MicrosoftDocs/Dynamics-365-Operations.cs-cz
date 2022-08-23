---
title: Sjednocené prostředí produktu
description: Tento článek popisuje integraci dat produktů mezi finančními a provozními aplikacemi a Dataverse.
author: t-benebo
ms.date: 06/23/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 89ef56510ec971ef97fc9eb5c80768527abf5f88
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288915"
---
# <a name="unified-product-experience"></a>Sjednocené prostředí produktu

[!include [banner](../../includes/banner.md)]



Pokud se obchodní ekosystém skládá z aplikace Dynamics 365, jako je například finance, Supply Chain Management a Sales, firmy tyto aplikace často používají ke zdrojování údajů o produktů. Důvodem je skutečnost, že tyto aplikace poskytují robustní produktovou infrastrukturu doplněnou sofistikovanými koncepty ocenění a přesnými daty o zásobách. Firmy, které používají externí systém správy životního cyklu produktu (PLM) pro výrobu dat produktu, mohou sdílet produkty z finančních a provozních aplikací do jiných aplikací Dynamics 365. Sjednocené prostředí produktu přináší integrovaný model dat produktu do Dataverse, takže všichni uživatelé aplikace včetně uživatelů Power Platform mohou využívat obsáhlá data o produktech přicházející z finančních a provozních aplikací.

Zde je datový model produktu z aplikace Sales.

![Datový model pro produkty v CE.](media/dual-write-product-4.jpg)

Zde je datový model produktů z finančních a provozních aplikací.

![Datový model pro produkty ve financích a provozu.](media/dual-write-products-5.jpg)

Tyto dva modely datových modelů produktů byly integrovány do Dataverse, jak je uvedeno níže.

![Datový model pro produkty v aplikacích Dynamics 365.](media/dual-write-products-6.jpg)

Mapování tabulky dvojího zápisu pro produkty bylo navrženo tak, aby data proudila pouze jednosměrně, a to v téměř reálném čase z finančních a provozních aplikací do Dataverse. Byla však vytvořena otevřená infrastruktura produktů, aby byla v případě potřeby obousměrná. I když ji můžete přizpůsobit, je to na vaše vlastní riziko, protože společnost Microsoft tento přístup nedoporučuje.

## <a name="templates"></a>Šablony

Informace o produktu obsahují všechny informace související s produktem a jeho definici, jako jsou například dimenze produktů nebo dimenze sledování a úložiště. Jak je ukázáno v následující tabulce, je vytvořena kolekce map tabulek pro synchronizaci produktů a souvisejících informací.

Finanční a provozní aplikace | Jiné aplikace Dynamics 365 | Popis
-----------------------|--------------------------------|---
[Všechny výrobky](mapping-reference.md#138) | msdyn_globalproducts | Tabulka Všechny produkty obsahuje všechny produkty, které jsou k dispozici ve finančních a provozních aplikacích, a to jak uvolněné produkty, tak i neuvolněné produkty.
[Uvolněné jedinečné produkty CDS](mapping-reference.md#213) | Produkt | Tabulka **Produkt** obsahuje sloupce, které definují produkt. Zahrnuje jednotlivé produkty (produkty s dílčím typem produktu) a varianty produktu. Následující tabulka zobrazuje mapování.
[Barvy](mapping-reference.md#170) | msdyn\_productcolors
[Konfigurace](mapping-reference.md#171) | msdyn\_productconfigurations
[Výchozí nastavení objednávky](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Kategorie produktu](mapping-reference.md#166) | msdyn_productcategories | Každá z kategorií produktů a informace o její struktuře a vlastnostech je obsažena v tabulce kategorie produktu.
[Přiřazení kategorií produktů](mapping-reference.md#167) | msdyn_productcategoryassignments | Chcete-li přiřadit produkt do kategorie, lze použít tabulku přiřazení kategorie produktu.
[Hierarchie kategorií produktů](mapping-reference.md#168) | msdyn_productcategoryhierarchies | Hierarchie produktů můžete použít k uspořádání produktů do kategorií nebo k jejich seskupení. Hierarchie kategorií jsou k dispozici v Dataverse prostřednictvím tabulky Hierarchie kategorií produktu.
[Role hierarchie kategorií produktů](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles | Hierarchie produktů lze použít pro různé role v D365 finance a provoz. Určují, která kategorie se použije v jednotlivých rolích, v nichž se používá tabulka role kategorie produktu.
[Výchozí nastavení pořadí produktů V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |
[Skupiny dimenzí produktu](mapping-reference.md#173) | msdyn\_productdimensiongroups | Skupina dimenzí produktu definuje, které dimenze produktu definují produkt.
[Barvy základního produktu](mapping-reference.md#187) | msdyn_sharedproductcolors | Tabulka **Sdílená barva produktu** označuje barvy, které může mít určitý základní produkt k dispozici. Účelem migrace tohoto konceptu do Dataverse je zachování konzistence dat.
[Konfigurace základního produktu](mapping-reference.md#188) | msdyn_sharedproductconfigurations | Tabulka **Sdílená konfigurace produktu** označuje konfigurace, které má určitý základní produkt k dispozici. Účelem migrace tohoto konceptu do Dataverse je zachování konzistence dat.
[Velikosti základního produktu](mapping-reference.md#190) | msdyn_sharedproductsizes | Tabulka **Sdílená velikost produktu** označuje velikosti, které může mít konkrétní základní produkt. Účelem migrace tohoto konceptu do Dataverse je zachování konzistence dat.
[Styly základního produktu](mapping-reference.md#191) | msdyn_sharedproductstyles | Tabulka **Sdílený styl produktu** označuje styly, které má určitý základní produkt k dispozici. Účelem migrace tohoto konceptu do Dataverse je zachování konzistence dat.
[Identifikované čárové kódy čísla produktu](mapping-reference.md#164) | msdyn\_productbarcodes | Čárové kódy produktů se používají k jednoznačné identifikaci produktů.
[Převody jednotek pro určité produkty](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Uvolněné produkty V2](mapping-reference.md#189) | msdyn\_sharedproductdetails | Tabulka **msdyn\_Sharedproductdetails** obsahuje sloupce z finančních a provozních aplikací, které definují produkt a obsahují finanční a řídící informace o produktu.
[Velikosti](mapping-reference.md#174) | msdyn\_productsizes
[Skupiny dimenze úložiště](mapping-reference.md#177) | msdyn_productstoragedimensiongroups | Skupina dimenze úložiště produktů představuje metodu, která se používá k definování umístění produktu ve skladu.
[Styly](mapping-reference.md#178) | msdyn\_productstyles
[Skupiny sledovací dimenze](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups | Skupina sledovací dimenze produktů představuje metodu použitou ke sledování produktu v zásobách.
[Jednotky](mapping-reference.md#219) | uoms
[Převody jednotek](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="integration-of-products"></a>Integrace produktů

V tomto modelu je produkt reprezentován kombinací dvou tabulek v Dataverse: **Produkt** a **msdyn\_sharedproductdetails**. Zatímco první tabulka obsahuje definici produktu (jedinečný identifikátor produktu, název produktu a popis), druhá tabulka obsahuje sloupce uložené na úrovni produktu. Kombinace těchto dvou tabulek se používá k definování výrobku podle konceptu skladové jednotky (SKU). Každý uvolněný produkt bude mít své informace v uvedených tabulkách (podrobnosti o produktu a sdíleném produktu). Chcete-li sledovat všechny produkty (uvolněné a neuvolněné), použije se tabulka **Globální produkty**.

Vzhledem k tomu, že produkt je reprezentován jako skladová jednotka, koncepty jedinečných produktů, základních produktů a variant produktů lze zaznamenat v Dataverse následujícím způsobem:

- **Produkty s podtypem** jsou produkty definované samy sebou. Není nutné definovat žádné dimenze. Příkladem je určitá kniha. Pro tyto produkty je vytvořen jeden řádek v tabulce **Produkt** a jeden řádek je vytvořen v tabulce **msdyn\_sharedproductdetails**. Není vytvořen žádný řádek produktové řady.
- **Základní produkty** se používají jako obecné výrobky, které obsahují definici a pravidla určující chování obchodních procesů. Na základě těchto definic mohou být vygenerovány jedinečné produkty, které jsou známy jako varianty produktu. Například tričko je základní produkt a může mít barvu a velikost jako dimenze. Varianty lze uvolnit s různými kombinacemi těchto dimenzí, jako je například malé modré triko nebo středně velké zelené triko. V rámci integrace je v tabulce produktů vytvořen jeden řádek na variantu. Tento řádek obsahuje specifické informace o variantách, jako jsou například různé dimenze. Obecné informace o produktu jsou uloženy v tabulce **msdyn\_sharedproductdetails**. (Tyto obecné informace se uchovávají v základním produktu.) Informace základního produktu se synchronizují s Dataverse, jakmile je vytvořen uvolněný hlavní produkt (před uvolněním variant).
- **Jedinečné produkty** odkazují na všechny produkty podtypu produktu a všechny varianty produktu.

![Datový model pro produkty.](media/dual-write-product.png)

V případě povolené funkce dvojího zápisu budou produkty z financí a provozu synchronizovány v dalších produktech Dynamics 365 ve stavu **Koncept**. Jsou přidány do prvního ceníku se stejnou měnou, jaká byla použita v aplikaci pro zapojení zákazníků, a používají abecední řazení v názvu ceníku. Jinými slovy se přidají k prvnímu ceníku v aplikaci Dynamics 365, která odpovídá měně právnické osoby, kde je produkt uvolněn ve finanční a provozní aplikaci. Pokud pro danou měnu neexistuje ceník, bude automaticky vytvořen a bude mu přiřazen produkt.

Aktuální implementace pluginů pro duální zápis, které přidružují výchozí ceník k jednotce, vyhledá měnu přidruženou k finanční a provozní aplikaci a najde první ceník v aplikaci Customer Engagement pomocí abecedního řazení názvu ceníku. Chcete-li nastavit výchozí ceník pro konkrétní měnu, pokud máte pro tuto měnu více ceníků, musíte aktualizovat název ceníku na název, který je v abecedním pořadí dříve než jakékoli jiné ceníky pro stejnou měnu. Pokud pro danou měnu nemá žádný ceník, vytvoří se nový.

Ve výchozím nastavení jsou produkty z finančních a provozních aplikací synchronizovány do ostatních aplikací Dynamics 365 ve stavu **Koncept**. Chcete-li synchronizovat produkt se stavem **Aktivní**, aby jej bylo možné přímo použít v nabídkách prodejních objednávek, je třeba vybrat následující nastavení: v části **Systém > Správa > Správa systému > Nastavení systému > karta Prodej** vyberte **Vytvořit produkty v aktivním stavu =Ano**.

Pokud jsou produkty synchronizovány, musíte zadat hodnotu pro pole **Prodejní jednotka** ve finanční a provozní aplikaci, protože je to povinné pole v prodeji.

Vytváření skupin produktů z Dynamics 365 Sales není podporováno synchronizací produktů s dvojím zápisem.

Synchronizace produktů probíhá z finanční a provozní aplikace do Dataverse. To znamená, že hodnoty sloupců tabulky produktu lze změnit v Dataverse, ale při spuštění synchronizace (při změně sloupce produktu ve finanční a provozní aplikaci) dojde k přepsání hodnot v Dataverse.

Finanční a provozní aplikace | Aplikace Customer Engagement |
---|---
[Uvolněné jedinečné produkty CDS](mapping-reference.md#213) | Produkt |
[Uvolněné produkty V2](mapping-reference.md#189) | msdyn_sharedproductdetails |
[Všechny výrobky](mapping-reference.md#138) | msdyn_globalproducts |

## <a name="product-dimensions"></a>Dimenze produktu

Dimenze produktu jsou vlastnosti, které identifikují variantu produktu. K definování variant produktu jsou mapovány do Dataverse také čtyři dimenze produktu (barva, velikost, styl a konfigurace). Následující ilustrace znázorňuje datový model pro dimenzi produktu Barva. Stejný model se použije pro Velikosti, Styly a Konfigurace.

![Datový model pro dimenze produktu.](media/dual-write-product-two.png)

Finanční a provozní aplikace | Aplikace Customer Engagement |
---|---
[Barvy](mapping-reference.md#170) | msdyn\_productcolors
[Velikosti](mapping-reference.md#174) | msdyn\_productsizes
[Styly](mapping-reference.md#178) | msdyn\_productstyles
[Konfigurace](mapping-reference.md#171) | msdyn\_productconfigurations

Pokud má produkt jiné dimenze produktu (například velikost a barvu základního produktu jako dimenze produktu), je každý jedinečný produkt (tj. každá varianta produktu) definován jako kombinace těchto dimenzí produktů. Například číslo produktu B0001 je velmi malé černé triko a číslo produktu B0002 je malé černé triko. V tomto případě jsou definovány existující kombinace dimenzí produktů. Například tričko z předchozího příkladu může být velmi malé a černé, malé a černé, střední a černé nebo velké a černé, ale nemůže být navíc velmi velké a černé. Jinými slovy se specifikují dimenze produktu, které může základní produkt, a varianty mohou být uvolněny na základě těchto hodnot.

Chcete-li sledovat dimenze produktu, které může mít základní produkt, budou vytvořeny a mapovány následující tabulky v Dataverse pro každou dimenzi produktu. Další informace viz [Přehled informací o produktech](../../../../supply-chain/pim/product-information.md).

Finanční a provozní aplikace | Aplikace Customer Engagement |
---|---
[Barvy základního produktu](mapping-reference.md#187) | msdyn_sharedproductcolors |
[Konfigurace základního produktu](mapping-reference.md#188) | msdyn_sharedproductconfigurations |
[Velikosti základního produktu](mapping-reference.md#190) | msdyn_sharedproductsizes |
[Styly základního produktu](mapping-reference.md#191) | msdyn_sharedproductstyles |
[Identifikované čárové kódy čísla produktu](mapping-reference.md#164) | msdyn\_productbarcodes |

## <a name="default-order-settings-and-product-specific-default-order-settings"></a>Výchozí nastavení objednávky a výchozí nastavení objednávky specifické pro produkt

Výchozí nastavení objednávky definuje pracoviště a sklad, odkud pocházející nebo kde jsou uloženy položky, minimální, maximální, násobná a standardní množství, která budou použita pro obchodování nebo řízení skladu, doby realizace, příznaky pro zastavení a metody příslibu objednávek. Tyto informace budou k dispozici v Dataverse pomocí výchozího nastavení objednávky a výchozí entity nastavení objednávky specifické pro produkt. Další informace o funkci naleznete v článku [Výchozí nastavení objednávky](../../../../supply-chain/production-control/default-order-settings.md).

Finanční a provozní aplikace | Aplikace Customer Engagement |
---|---
[Výchozí nastavení objednávky](mapping-reference.md#172) | msdyn_productdefaultordersettings |
[Výchozí nastavení pořadí produktů V2](mapping-reference.md#175) | msdyn_productspecificdefaultordersettings |

## <a name="unit-of-measure-and-unit-of-measure-conversions"></a>Převody měrných jednotek

Měrné jednotky a odpovídající převod jsou k dispozici v Dataverse podle datového modelu zobrazeného v diagramu.

![Datový model pro měrnou jednotku.](media/dual-write-product-three.png)

Pojem měrné jednotky je integrován mezi finančními a provozními aplikacemi a jinými aplikacemi Dynamics 365. Pro každou třídu jednotek ve finanční a provozní aplikaci se v aplikaci Dynamics 365 vytvoří skupina jednotek, která obsahuje jednotky náležející ke třídě jednotek. Výchozí základní jednotka je také vytvořena pro každou skupinu jednotek.

Finanční a provozní aplikace | Aplikace Customer Engagement |
---|---
[Převody jednotek pro určité produkty](mapping-reference.md#176) | msdyn_productspecificunitofmeasureconversions |
[Jednotky](mapping-reference.md#219) | uoms
[Převody jednotek](mapping-reference.md#199) | msdyn_ unitofmeasureconversions

## <a name="initial-synchronization-of-units-data-matching-between-finance-and-operations-and-dataverse"></a>Počáteční synchronizace párování dat jednotek mezi finančními a provozními aplikacemi a Dataverse

### <a name="initial-synchronization-of-units"></a>Počáteční synchronizace jednotek

Když je povolen dvojí zápis, jsou jednotky z finančních a provozních aplikací synchronizovány do aplikací Dynamics 365. Skupiny jednotek synchronizované z finančních a provozních aplikací v Dataverse mají sadu příznaků, která označuje, že jsou „externě udržované“.

### <a name="matching-units-and-unit-classesgroups-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Odpovídající jednotky a data tříd/skupin jednotek z finančních a provozních aplikací a jiných aplikací Dynamics 365

Nejprve je důležité poznamenat, že klíč integrace pro jednotku je msdyn_symbol. Tato hodnota musí být proto jedinečná v aplikaci Dataverse nebo v jiných aplikacích Dynamics 365. Protože v jiných aplikacích Dynamics 365 jsou to údaje „ID skupiny jednotek“ a „Název“, které definují jedinečnost jednotky, musíte zvážit různé scénáře pro spárování dat jednotek mezi finančními a provozními aplikacemi a Dataverse.

Pro jednotky spárované/překrývající se ve finančních a provozních aplikacích a jiných aplikacích Dynamics 365:

+ **Jednotka patří do skupiny jednotek v jiných aplikacích Dynamics 365, které odpovídají přidružené třídě jednotek ve finančních a provozních aplikacích**. V takovém případě musí být sloupec msdyn_symbol v ostatních aplikacích Dynamics 365 vyplněn symbolem jednotky z finančních a provozních aplikací. Proto, když budou data spárována a skupina jednotek bude nastavena jako „externě udržovaná“ v jiných aplikacích Dynamics 365.
+ **Jednotka patří do skupiny jednotek v jiných aplikacích Dynamics 365, které neodpovídají přidružené třídě jednotek ve finančních a provozních aplikacích (žádná existující třída jednotek ve finančních a provozních aplikacích pro třídu jednotek v jiných aplikacích Dynamics 365).** V takovém případě musí být msdyn_symbol vyplněn náhodným řetězcem. Pamatujte, že tato hodnota musí být jedinečná v aplikacích Dynamics 365.

Pro jednotky a třídy jednotek ve finančních a provozních aplikacích neexistující v jiných aplikacích Dynamics 365:

Jako součást dvojího zápisu jsou skupiny jednotek z finančních a provozních aplikací a jejich odpovídající jednotky vytvořeny a synchronizovány v jiných aplikacích Dynamics 365 a Dataverse a skupina jednotek bude nastavena jako „externě udržovaná“. Není nutné provádět žádné dodatečné zaváděcí úsilí.

Pro jednotky v jiných aplikacích Dynamics 365, které neexistují ve finančních a provozních aplikacích:

Sloupec msdyn_symbol musí být vyplněn pro všechny jednotky. Jednotky mohou být vždy vytvořeny ve finančních a provozních aplikacích v odpovídající třídě jednotek (pokud existuje). Pokud třída jednotek neexistuje, musí být nejprve vytvořena (všimněte si, že nemůžete vytvořit třídu jednotek ve finančních a provozních aplikacích, kromě možnosti rozšíření, pokud rozšiřujete výčet) a spárována s jinou skupinou jednotek aplikací Dynamics 365. Poté můžete vytvořit jednotku. Symbol jednotky ve finančních a provozních aplikacích musí být msdyn_symbol dříve specifikovaný v jiných aplikacích Dynamics 365 pro jednotku.

## <a name="product-policies-dimension-tracking-and-storage-groups"></a>Zásady produktu: dimenze, sledování a skupiny úložišť

Zásady produktu jsou sady zásad, které se používají pro definování produktů a jejich charakteristik v zásobách. Jako zásady produktu lze nalézt skupinu dimenzí produktu, skupinu dimenzí sledování produktu a skupinu dimenzí úložiště.

Finanční a provozní aplikace | Aplikace Customer Engagement |
---|---
[Skupiny dimenzí produktu](mapping-reference.md#173) | msdyn\_productdimensiongroups |
[Skupiny dimenze úložiště](mapping-reference.md#177) | msdyn_productstoragedimensiongroups |
[Skupiny sledovací dimenze](mapping-reference.md#179) | msdyn_producttrackingdimensiongroups |

## <a name="product-hierarchies"></a>Hierarchie výrobků

Finanční a provozní aplikace | Aplikace Customer Engagement |
---|---
[Přiřazení kategorií produktů](mapping-reference.md#167) | msdyn_productcategoryassignments |
[Hierarchie kategorií produktů](mapping-reference.md#168) | msdyn_productcategoryhierarchies |
[Role hierarchie kategorií produktů](mapping-reference.md#169) | msdyn_productcategoryhierarchyroles |

## <a name="integration-key-for-products"></a>Klíč integrace pro produkty

Pro jednoznačnou identifikaci produktů mezi Dynamics 365 Finance a produktů v Dataverse se používá klíč integrace.
U produktů je **(productnumber)** jedinečným klíčem, který identifikuje produkt v Dataverse. Je tvořen zřetězením: **(company, msdyn_productnumber)**. **Company** označuje právnickou osobu ve financích a provozu a **msdyn_productnumber** označuje číslo produktu pro specifický produkt ve finanční a provozní aplikaci.

Pro uživatele ostatních aplikací Dynamics 365 je produkt identifikován v uživatelském rozhraní pomocí **msdyn_productnumber** (všimněte si, že popisek sloupce je **číslo produktu**). Ve formuláři produktu jsou zobrazeny jak company, tak i msydn_productnumber. Ve sloupci (productnumber) však není zobrazen jedinečný klíč produktu.

Pokud vytváříte aplikace v Dataverse, měli byste věnovat pozornost použití **productnumber** (jedinečné ID produktu) jako klíče integrace. Nepoužívejte **msdyn_productnumber**, protože není jedinečné.

## <a name="initial-synchronization-of-products-and-migration-of-data-from-dataverse-to-finance-and-operations"></a>Počáteční synchronizace produktů a migrace dat z Dataverse do financí a provozu

### <a name="initial-synchronization-of-products"></a>Počáteční synchronizace produktů

Když je povolen dvojí zápis, jsou produkty z finančních a provozních aplikací synchronizovány do Dataverse a jiných aplikací Customer Engagement. Produkty vytvořené v Dataverse a jiných aplikacích Dynamics 365 před uvolněním dvojího zápisu nebudou aktualizovány ani spárovány s daty produktu z finančních a provozních aplikací.

### <a name="matching-product-data-from-finance-and-operations-and-other-dynamics-365-apps"></a>Párování dat produktu z finančních a provozních aplikací a dalších aplikací Dynamics 365

Pokud jsou stejné produkty uchovávány (překrývání a spárování) ve finanční a provozní aplikaci a Dataverse a v jiných aplikacích Dynamics 365 při povolování dvojího zápisu, dojde k provedení synchronizace produktů z finančních a provozních aplikací a duplicitní řádky se zobrazí v Dataverse pro stejný produkt.
Chcete-li se vyhnout předchozí situaci, pokud ostatní aplikace Dynamics 365 obsahují produkty, které se překrývají a shodují s financemi a provozem, musí správce povolující dvojí zapisování spustit sloupce **Společnost** (například: "USMF") a **msdyn_productnumber** (příklad: 1234:Black:S) před tím, než dojde k synchronizaci produktů. Jinými slovy, tyto dva sloupce v produktu v Dataverse musejí být vyplněny příslušnou společností ve finanční a provozní aplikaci, se kterou musí být výrobek spárován, a se svým číslem produktu.

Pokud je synchronizace povolena a probíhá, budou produkty z finančních a provozních aplikací synchronizovány se spárovanými produkty v aplikaci Dataverse a v dalších aplikacích Dynamics 365. To platí pro jedinečné produkty i varianty produktu.

### <a name="migration-of-product-data-from-other-dynamics-365-apps-to-finance-and-operations"></a>Migrace dat produktu z dalších aplikací Dynamics 365 do finančních a provozních aplikací

Pokud jiné aplikace Dynamics 365 obsahují produkty, které nejsou přítomny ve finanční a provozní aplikaci, může správce nejprve použít **EcoResReleasedProductCreationV2Entity** pro import těchto produktů ve finanční a provozní aplikaci. A za druhé, spárujte data produktu z finanční a provozní aplikace a dalších aplikací Dynamics 365, jak je popsáno výše.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

