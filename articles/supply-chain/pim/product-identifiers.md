---
title: Identifikátory produktu
description: Toto téma obsahuje informace o různých typech identifikátorů produktu a vysvětluje přidání identifikátorů produktu do dat produktu.
author: cvocph
manager: AnnBe
ms.date: 03/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductEntityIdentifierCode, EcoResProductListPage, EcoResProductDetailsExtended, EcoResProductVariantsPerCompany
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 0aa8baf5802ccdd9a502e2a7d291a76fc4afe932
ms.sourcegitcommit: d91d96c98b31ae59bc82ec91efbb7da86ffb25fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172018"
---
# <a name="product-identifiers"></a>Identifikátory produktu

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o různých typech identifikátorů produktu a vysvětluje přidání identifikátorů produktu do dat produktu.

Při práci s produkty v dílně nebo ve skladu v aplikaci Microsoft Dynamics ERP nebo Microsoft Dynamics CRM musíte mít dobrou strategii pro identifikaci těchto produktů a variant produktu.

## <a name="unique-product-numberproduct-id"></a>Jedinečné číslo produktu/ID produktu

V aplikaci Dynamics 365 Supply Chain Management je primárním identifikátorem produktu číslo produktu (tedy jedinečné ID produktu). Toto číslo lze generovat automaticky podle číselné řady, nebo ho lze ručně přiřadit k produktu. Pro varianty produktu lze definovat čísla pomocí šablony klasifikace produktu.

V mnoha případech není číslo produktu původně vytvořeno v modulu Dynamics 365 Supply Chain Management. Namísto toho je přidružen k produktu v systému správy (PLM) životního cyklu produktu nebo systém pro správu dat produktu (PDM). V takovém případě používáte data entity k importu produktů a variant produktu. Aplikace Supply Chain Management pak tato čísla použije ve všech operacích.

Při implementaci aplikace Supply Chain Management je třeba obzvláště zvážit strategii čísel produktů. Systém číslování zboží vylepšuje toky logistiky a pomáhá předcházet chybám. Dobrý identifikátor produktu může mít nejvýše 15 znaků. V optimálním případě má méně než 10 znaků a obsahuje více než pět klasifikačních znaků. Můžete také použít vyhledávací pro účely rychlého vyhledávání. Vyhledávací název je další název představující klasifikaci produktu.

Pokud použijete Common Data Service, je číslo produktu v modulu Supply Chain Management také číslo produktu v poli Common Data Service. Varianty produktu jsou synchronizovány do Common Data Service jako odlišné produkty.

## <a name="item-number-and-product-dimensions"></a>Dimenze čísla položky a produktů

Číslo položky je identifikátor produktu používaný určitou právnickou osobu. Číslo položky by v ideálním případě mělo být shodné s číslem produktu. Pokud se liší klasifikace za právnickou osobu, bude náročné sledovat produkt v řetězci dodávek a bude přidáno zatěžující přeznačení a odkazování na procesy. Tento model jsme zachovali pro zajištění kompatibility se starší verzí (to znamená, aplikaci Microsoft Dynamics AX 2009 a dřívější). Doporučujeme však eliminaci identifikátorů, které jsou specifické pro právnické osoby, kdykoli je to možné, a místo toho použít číslo jedinečného produktu jako primární identifikátor.

Kromě toho nelze variantu produktu jedinečně identifikovat podle čísla položky. Vždy vyžaduje kombinaci čísla položky a všech dimenzí produktu, které jsou definovány v základním produktu. Tento požadavek se může stát těžkopádným a může zpomalit procesy identifikace. Z toho důvodu doporučujeme také, abyste vždy, když je to možné, použili jedinečné číslo produktu místo číslo položky.

Spousta stránek jako primární identifikátory stále ještě používá dimenze produktu a číslo položky. Čísla produktů však lze použít při vyhledávání. V okně **Prodej a marketing** &gt; **Nastavení** &gt; **Vyhledávání** &gt; **Parametry hledání** můžete změnit vyhledávací kód tak, aby používal čísla produktů místo čísla položky strategie primárního vyhledávání. Nastavíte-li možnost **povolit vyhledávání pro vyhledávání produktu** na **Ano**, vyhledávání zobrazí pouze nejen hlavní produkty, ale varianty produktu. Další informace uvádí téma [Vyhledávání produktů a variant produktu během zadávání objednávky](search-products-product-variants.md)

Kromě toho budete moci vyhledávat a filtrovat číslo produktu, název produktu a popis a dimenze produktu a ID varianty produktu. Pokud zvolíte variantu, zvolí se související číslo položky a všechna ID dimenze produktu. Můžete tedy snadněji vyhledat a zvolit správnou variantu. Toto nastavení se důrazně doporučuje při použití variant produktu a jedinečného čísla produkt jako primárních identifikátorů produktů. Jedinou výjimkou může být odvětví módy, kde často obchodní procesy vyžadují volbu hlavního produktu před výběrem varianty. Před implementací systému číslování byste měli pozorně vyhodnotit tuto možnost.

> [!NOTE]
> Číslo položky produktu nelze změnit, pokud pro tento produkt existuje nejméně jedna transakce.

## <a name="product-name-and-description"></a>Název a popis produktu

Název produktu a popis jsou identifikátory produktu, čitelné pro osoby, a lze je udržovat ve více jazycích. Ve výchozím nastavení zobrazuje klient Supply Chain Management všechny informace o produktu ve výchozím jazyce společnosti, nikoli v jazyce uživatele. Přeložené názvy a popisy produktů se však používají ve veškeré komunikaci s odběrateli a dodavateli. Překlady jsou založeny na kódu jazyka účtů odběratelů a dodavatelů.

Pro varianty produktu lze generovat název produktu pomocí šablony klasifikace produktu. Protože neexistuje žádný požadavek na jedinečnost názvů produktu, může se objevit více produktů, které mají stejné názvy.

## <a name="product-and-item-search-names"></a>Vyhledávací názvy produktů a položek

Supply Chain Management nabízí sekundární vyhledávací název pro produkty a pro položky (uvolněné produkty). Tento vyhledávací název nemusí být jedinečný a lze ho změnit po vytvoření produktu nebo varianty produktu. Doporučujeme použít vyhledávací název pro hledání produktů podle kategorie. Vyhledávací názvy umožňují rychlé vyhledávání, zejména v prodejních a nákupních procesech.

Vyhledávací název může obsahovat odběratele nebo ID produktu dodavatele, nebo některé jiné externí ID produktu, pokud je toto externí ID primárním vyhledávacím kritériem pro produkt.

## <a name="external-product-identifiers-customer-and-vendor-identifiers"></a>Externí identifikátory produkut (identifikátory odběratele a dodavatele)

Pro uvolněné produkty můžete udržovat čísla položek, názvy položek a popisy položky, používané odběratele nebo dodavatele. Odkazy jsou zobrazeny v externích dokumentech, například prodejních objednávkách, nákupních objednávkách, dodacích listech a fakturách. V aktuální verzi aplikace Supply Chain Management se nezobrazí externí odkazy na stránkách základních operací. Jedinou výjimkou je číslo položky dodavatele. Toto číslo je zobrazeno v dialogovém okně **Informace o produktu**, pokud je pro uvolněný produkt definován dodavatel.

Můžete spravovat externí identifikátory produktu podle uvolněného produktu, varianty uvolněného produktu, odběratele nebo skupiny odběratelů, či dodavatele nebo skupiny dodavatelů.

Na stránce **uvolněné produkty** proveďte jeden z následujících kroků.

- Pro odběratele na kartě **prodávat** ve skupině **Související informace** vyberte **Externí popis položky**.
- Pro dodavatele na kartě **Nákup** ve skupině **Související informace** vyberte **Popis externí položky**.

Na stránce **Externí popisy položek** můžete přidružit číslo položky odběratele nebo dodavatele k uvolněnému produktu. Toto přiřazení je nutné provést pro každou právnickou osobu. Lze zaznamenat následující informace. Bohužel popisky jsou v současné verzi aplikace Supply Chain Management mírně zavádějící. Tyto štítky však můžete změnit v příští verzi.

| Pole | Odpovídající informace o odběrateli | Odpovídající informace o dodavateli |
|-------|------------------------------------|----------------------------------|
| Číslo externí položky | Číslo položky odběratele. | Číslo položky dodavatele |
| popis | Název, který odběratel přiřadil k položce | Název, který dodavatel přiřadil k položce |
| Externí text položky | Popis položky odběratele | Popis položky dodavatele |

Používá-li více odběratelů nebo dodavatelů stejná čísla položek (například v případě nákupního přidružení nebo velkoobchodní skupiny), můžete vytvořit skupiny odběratelů nebo dodavatelů, chcete-li zjednodušit správu informací o externích produktech.

- Pro skupiny odběratelů přejděte na **Prodej** &gt; **nastavení** &gt; **položky** &gt; **externí popis položky** k vytváření a údržbě skupin a jejich souvisejících čísel položek. Pokud chcete přiřadit odběratele ke skupině, přejděte na **Pohledávky** &gt; **Odběratelé** &gt; **Všichni odběratelé** a poté na pevné záložce **Výchozí nastavení prodejních objednávek** určete hodnotu v poli **Položka – Skupina odběratelů**.
- Pro skupiny dodavatelů přejděte na **Zásobování a zdroje** &gt; **nastavení** &gt; **Skupina popisu externí položky** k vytváření a údržbě skupin a jejich souvisejících čísel položek. Pokud chcete přiřadit dodavatele ke skupině, přejděte na **Pohledávky** &gt; **Dodavatelé** &gt; **Všichni dodavatelé** a poté na pevné záložce **Výchozí nastavení nákupních objednávek** určete hodnotu v poli **Položka – Skupina dodavatelů**.
 
## <a name="bar-codes"></a>Čárové kódy

Pokud chcete použít k určení výrobků skener čárového kódu, identifikátor produktu musí splňovat požadavky standardního čárového kódu, který se používá. Proto čárové kódy neobsahují obvykle číslo suroviny, ale číslo vytvořené výhradně pro zvolené technologie čárového kódu. Lze spravovat více čárových kódů podle typu čárového kódu. Můžete dokonce i přidružit stejný čárový kód k více produktům a poté vybrat aktivní skutečné přidružení po naskenování čárového kódu.

Před definováním čárových kódů lze definovat jedno nebo více nastavení čárového kódu. Nastavení čárových kódů může pomoci ověřit, zda čárové kódy odpovídají požadovaným pokynům a zda mohou být efektivně vytištěny a naskenovány. Také můžete udržovat speciální čárové kódy pro konkrétní množství produktu.

Doporučujeme použít nastavení čárového kódu pro správu kódů globálního čísla obchodní položky nebo mezinárodní čísla zboží.

Chcete-li spravovat čárové kódy, zvolte na stránce **Uvolněné produkty** na kartě **Správa skladu** ve skupině **Sklad** možnost **Čárové kódy**.

## <a name="gtin-codes"></a>Kódy GTIN

V elektronickém obchodování je důležité, aby všechny strany mluvily společným jazykem a odkazovaly na produkty pomocí společné sady identifikátorů. Proto některá odvětví spoléhají na [GTIN](https://www.gs1.org/id-keys/gtin), což je globální systém čísel položek zprostředkovaný GS1.

Doporučujeme udržovat číslo GTIN jako čárový kód. Lze ho však dále udržovat také na stránce **Položka – GTIN**. Chcete-li otevřít tuto stránku, zvolte na stránce **Uvolněné produkty** na kartě **Správa skladu** ve skupině **Sklad** možnost **Kódy GTIN**. Všimněte si, že není GTIN udržováno jako globální číslo. Namísto toho se spravuje podle právnické osoby.

V modulu Supply Chain Management lze určit varianty balení pro skladové operace definováním konkrétní měrné jednotky. Například položka by mohla být uložena po kusech, sadách po šesti, v zásobnících po 18 nebo na plných paletách. Konkrétní jednotka měření bude určena pro každou z těchto varianty balení. Vzhledem k tomu, že GTIN obvykle souvisí s jednotkou balení produktů, stránka **Položka – GTIN** stránce umožňuje spravovat více kódů GTIN pro produkt a měrnou jednotku. Nemůžete však použít stejný kód GTIN opakovaně pro různé položky nebo varianty produktu právnické osoby.

Chcete-li spravovat **Kódy GTIN**, zvolte na stránce **Uvolněné produkty** na kartě **Správa skladu** ve skupině **Sklad** možnost **GTIN**.

## <a name="external-codes"></a>Externí kódy

Externí kódy mohou být definovány pro mnoho entit. Například je možné definovat externí kódy pro identifikaci produktů a uvolněných produktů. Tyto externí kódy lze použít k přiřazení statistických kódů nebo daňových kódů k uvolněným produktům a uvolněným variantám produktu. Externí kódy jsou definovány podle právnické osoby a typu kódu. Musí být jedinečné podle právnické osoby, typu kódu a odkazu na tabulku.

Bohužel neexistuje standardní funkce, která by vám umožnila vyhledávání produktů podle externích kódů.

## <a name="data-entities-that-are-used-to-import-and-export-product-identifiers"></a>Datové entity, které se používají k importu a exportu identifikátorů produktu

| Název entity | Identifikátory importu | Identifikátory exportu | Poznámky |
|-------------|--------------------|--------------------|----------|
| Produkty V2 | Číslo produktu, vyhledávací název produktu, název produktu, popis produktu | Číslo produktu, vyhledávací název produktu, název produktu, popis produktu | V závislosti na nastavení entity a číselné řady pro číslo produktu lze automaticky vytvořit číslo produktu v okamžiku importu. |
| Varianty produktu | Číslo produktu, vyhledávací název produktu, název produktu, popis produktu | Číslo produktu, vyhledávací název produktu, název produktu, popis produktu | V závislosti na šabloně klasifikace produktu může být číslo výrobku automaticky vytvořeno při importu. Můžete však importovat všechna jedinečná číslo výrobku a toto číslo produktu nemusí vycházet ze struktury šablony klasifikace produktu. |
| Překlady produktu | Název produktu, popis produktu | Název produktu, popis produktu | Tato entita přepíše libovolný jazyk. Všimněte si, že při když je přepsán název nebo popis jazyka primární právnické osoby, název a popis produktu se změní. |
| Tvorba uvolněného produktu V2 | Číslo položky, číslo produktu, vyhledávací název položky| Číslo položky, číslo produktu, vyhledávací název položky, vyhledávací název produktu, název produktu | Tato entita může být složitá při použití číselných řad během vytváření nových uvolněných produktů. Vliv má číselná řada **č. položky** i **číslo produktu**. Číselná řada **Číslo položky** však platí pro právnickou osobu, zatímco číselná řada **číslo produktu** je globální. Proto nedoporučujeme používat číselnou řadu **Číslo položky** při nasazení nových uvolněných produktů. Samozřejmě při použití entity pro uvolnění existujícího produktu musí být číslo produktu uvedeno v entitě. Další informace naleznete v tématu "Číselné řady produktů a položek" v tomto tématu. |
| Uvolněné varianty produktu | Číslo položky, dimenze produktu, číslo produktu | Číslo produktu, vyhledávací název produktu, název produktu, popis produktu, dimenze produktu | Stejně jako entit **varianty produktu** i tato entita slouží k vytvoření nových produktů, které mají stejnou šablonu klasifikace produktu nebo číslo produktu pro variantu. |
| Popisy externích položek pro odběratele | Číslo položky odběratele položky jméno zákazníka, popis odběratele, účtu odběratele | Číslo položky odběratele položky jméno zákazníka, popis odběratele, účtu odběratele | Skupinu odběratelů (například přidružení kupujícího) lze sloučit do jedné skupiny pomocí entity **Skupiny odběratelů popisu externí položky**. |
| Popis externích položek pro dodavatele | Číslo položky dodavatele, název položky dodavatele, popis dodavatele, účet dodavatele | Číslo položky dodavatele, název položky dodavatele, popis dodavatele, účet dodavatele | Skupinu dodavatelů (například prodejní asociaci nebo průmyslovou organizaci) lze sloučit do jedné skupiny pomocí entity **Skupiny dodavatelů popisu externí položky**. |
| Čárový kód položky | Čárový kód | Čárový kód | Všimněte si, že při importu musíte odkazovat na nastavení čárového kódu, který je definován v cílovém systému. Importované odkazy čárového kódu jsou ověřovány proti nastavení čárového kódu a jsou odmítnuty, pokud neodpovídají požadavkům definovaným v nastavení čárového kódu. |
| Externí kódy pro uvolněné produkty | Externí kód | Externí kód, třídy externího kódu, číslo položky | Externí kódy jsou podle právnické osoby. Pro import musíte odkazovat na definovaný kód třídy. Importujte třídy kódu pomocí entity **Třídy externího kódu pro uvolněné produkty**. |
| Externí kódy pro uvolněné varianty produkty | Externí kód | Externí kód, třídy externího kódu, číslo položky, dimenze produktu | Externí kódy jsou podle právnické osoby. Pro import musíte odkazovat na definovaný kód třídy. Importujte třídy kódu pomocí entity **Třídy externího kódu pro uvolněné produkty**. Tato entita odkazuje na varianty produktu podle čísla položky a dimenze produktu. |
| Exportovat kódy pro uvolněné varianty produktu podle identifikátoru čísla produktu | Externí kód | Externí kód, třídy externího kódu, číslo produktu | Externí kódy jsou podle právnické osoby. Pro import musíte odkazovat na definovaný kód třídy. Importujte třídy kódu pomocí entity **Třídy externího kódu pro uvolněné produkty**. Tato entita odkazuje na varianty produktu podle čísla produktu varianty. (Od další hlavní verze) |
| Číslo GTIN | Nelze použít | Nelze použít | V současné době neexistuje žádná konkrétní entita, která slouží k importu a exportu kódy GTIN. Doporučujeme namísto toho používat entitu **Čárový kód položky**. |
| Entita identifikátoru Common Data Service pro entitu produktu | Nelze použít | Číslo položky, vyhledávací název položky, vyhledávací název produktu, číslo položky dodavatele, odběratele, číslo položky, externí kódy, kódy GTIN, čárové kódy | Tato entita zkonsoliduje všechny identifikátory do jednoho datového modelu tak, aby bylo možné použít jedno rozhraní ke snadnému exportu všech identifikátorů a jejich souvisejících typů. Použijte entitu **Kódy identifikátoru entity produktu** pro export identifikačních kódů a popisů. Použijte entitu **Rozsah identifikátoru entity produktu** pro export dalších informací o rozsahu do identifikátoru, jako jsou například strana, právnická osoba, množství nebo jednotka. |

### <a name="product-and-item-number-sequences"></a>Číselné řady produkt a položka

Můžete definovat dvě různé číselné řady:

- Číselná řada **Číslo produktu** pro globální číslo produktu
- Číselná řada **Číslo položky** pro číslo položky podle právnické osoby

> [!NOTE]
> Měli byste použít číslo položky jako samostatný identifikátor pouze tehdy, když migrujete různé právnické osoby z různých zdrojů s různými systémy číslování. Měli byste se vždy snažit použít identifikátor produktu, který je jedinečný pro všechny právnické osoby. Proto je třeba nastavit možnost **Ruční** na **Ano** pro číselnou řadu **Číslo položky**. Tímto způsobem bude číslo položky vycházet z čísla produktu při vytvoření. Pokud modul Supply Chain Management není vedoucí systém nových čísel produktů, je třeba nastavit možnost **Ruční** na **Ano** pro číselné řady **č. položky** i **číslo produktu**.

Použijete-li entitu **Tvorba uvolněného produktu V2** k vytvoření produktů, mohou mnohá nastavení ovlivnit použití číselných řad při vytvoření čísla položky a čísla produktu:

- Nastavení číselné řady **Číslo produktu**
- Nastavení číselné řady **Číslo položky**
- Mapování čísla položky 
- Mapování čísla produktu

Následující tabulka obsahuje přehled výsledků importu a ručního vytvoření při konkrétní kombinace číselné řady a nastavení mapování polí.

| Číselná řada čísla produktu | Číselná řada čísel položky | Mapování čísla položky | Mapování čísla produktu | Výsledek importu entity | Výsledek ručního vytvoření | Závěr |
|--------------------------------|-----------------------------|----------------------------|-------------------------------|-------------------------|----------------------------|-----------|
| Je ruční = Ne | Je ruční = Ne | Žádné mapování | Žádné mapování | Čísla produktu používají číselnou řadu **Číslo produktu**. Čísla položek používají číselnou řadu **Číslo produktu**. | Čísla produktu používají číselnou řadu **Číslo produktu**. Čísla položek používají číselnou řadu **Číslo produktu**. | S touto konfigurací budou čísla produktů následovat po číselné řadě produktů a čísla položek budou následovat po číselné řadě položek. Tato konfigurace však nebude fungovat v případě, že existuje více než jedna položka (řádek), která má být importována. |
| Je ruční = Ne | Ruční = Ano | Automaticky vygenerovat | Žádné mapování | Číslování produktů i položek používají číselnou řadu **Číslo položky**. | Číslování produktů i položek používají číselnou řadu **Číslo produktu**. | Číslování produktů i položek používá číselnou řadu produktu. Jedná se o doporučený postup při importu nebalených produktů s použitím datové entity Tvorba uvolněného produktu V2. |
| Je ruční = Ne | Ruční = Ano | Žádné mapování | Žádné mapování | Číslování produktů i položek používají číselnou řadu **Číslo produktu**. | Číslování produktů i položek používají číselnou řadu **Číslo produktu**. | Číslování produktů i položek používá číselnou řadu produktu. Tato konfigurace však nebude fungovat v případě, že existuje více než jedna položka (řádek), která má být importována. |
| Ruční = Ano | Nelze použít | Nelze použít | Automaticky vygenerovat | Obdržíte následující chybovou zprávu: Nelze detekovat číselnou řadu. | Podle číselné řady **Číslo položky** | Toto nastavení není podporováno pro import. |

## <a name="product-entity-identifier-export-all-product-identifiers"></a>Identifikátor entity produktu (exportovat všechny identifikátory produktu)

Model identifikátoru entity produktu byl vytvořen proto, aby bylo možné zřídit verzi 1.0 CDS se všemi identifikátory, které se používají pro účely odkazování na produkt. Aby ye tato úloha zjednodušila, budou všechny identifikátory agregovány do jedné globální tabulky identifikátoru, aby je bylo možné exportovat jako jeden model. Všimněte si, že tato verze systému CDS nepoužívá model identifikátorů produktu. Proto má entita **Entita identifikátoru Common Data Service entity produktu** a tento proces omezené praktické použití a v budoucnu pravděpodobně dojde k jejich změně.

Tabulka identifikátorů produktu je globální tabulka, která se vytváří ze všech referenčních tabulek hlavní právnické osoby prostřednictvím opakované dávkové úlohy. Je nutné vybrat právnickou osobu a hierarchii kategorií produktu jako definici rozsahu hlavního globálního produktu. Generování tabulky globálních identifikátorů produktu je omezeno na produkty, které byly vydány pro vybranou právnickou osobu, a produkty, které jsou součástí hierarchie produktů, která je vybrána pro roli **Common Data Service** v produktu hierarchie kategorií.

Tento proces předpokládá, že hlavní data produktů jsou primárně udržována v jedné centrální právnické osobě. (Tato právnická osoba však může být virtuální právnická osoba, která se používá pouze k udržování globálních hlavních dat.)

Takto se konfiguruje prostředí:

1. Vybrat hierarchii kategorie pro CDS. Na stránce **Přidružení role hierarchie kategorií**, pokud není přidružena žádná hierarchie k roli **Common Data Service**, je nutné vytvořit nové přidružení. Vyberte roli **Common Data Service** a potom přidružte hierarchie kategorií představující nabídku produktů, které mají být synchronizovány do CDS.
2. Vyberte právnickou osobu pro globální hlavní data produktu. Na stránce **parametry modulu řízení informací o produktu** na kartě **Atributy produktu** vyberte hlavní společnost, kde jsou primárně zachovány identifikátory produktů a položek.
3. Definování typů kódů identifikátorů, které mají být exportovány. Přejděte na **řízení informací o produktech** &gt; **nastavení** &gt; **Kódy identifikátoru produktu**. Pro vygenerování typů kódů identifikátoru vyberte **Generovat kódy**. Pro každý typ identifikace, která je nalezena ve vybrané právnické osobě je generována položka typu kódu.

    Všimněte si, že pro čárové kódy se kód typu generuje pro každé nastavení čárového kódu. Pro každou třídu externího kódu je generován typ kódu.

    Nyní můžete spravovat seznam typů kódů. Můžete změnit kód, název a popis. Můžete také odstranit typy kódů. Typy kódů, které odstraníte, nebudou použity k naplnění globálních tabulek identifikátorů entity produktu.

4. Po ukončení definování typů identifikátor kódu identifikátoru produktů můžete vytvořit identifikátory v globální tabulce spuštěním úlohy **Vytvořit identifikátory entity produktu** na stránce **Kódy identifikátoru entity produktu**. Tuto úlohu byste měli spustit v dávce. Tato úloha by měla být nastavena jako periodická dávková úloha, aby byla tabulka vyplněna podle nových položek.

Nyní můžete použít datové entity **Entita identifikátoru Common Data Service entity produktu**, **Kód identifikátoru entity produktu** a **Rozsah identifikátoru entity produktu** za účelem exportu identifikátorů pro jakýkoliv cílový systém.

## <a name="related-topic"></a>Související téma

[Vyhledávání produktů a variant produktu během zadávání objednávky](search-products-product-variants.md)
