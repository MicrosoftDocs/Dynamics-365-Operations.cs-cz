---
title: Vyhledávání produktu a zákazníka v pokladním místě (POS)
description: Toto téma poskytuje přehled vylepšení, která byla provedena v aplikaci Dynamics 365 Commerce ohledně funkce vyhledávání produktu a vyhledávání zákazníka.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 1de8373471ff8187bd476305c9ed0b26beaa52d5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965271"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Vyhledávání produktu a zákazníka v pokladním místě (POS)

[!include [banner](includes/banner.md)]

Moderní pokladní místo (MPOS) a cloudové pokladní místo (CPOS) poskytují snadno použitelnou funkci vyhledávání produktů a zákazníků. Panel vyhledávání je vždy k dispozici v horní části oken MPOS a CPOS, aby zaměstnanci mohli rychle vyhledat produkty a zákazníky.

Zaměstnanci mohou vyhledávat produkty v katalozích, které souvisejí s aktuálním obchodem. Mohou také vyhledávat produkty v katalozích, které souvisejí s jiným obchodem ve společnosti. Proto pokladníci mohou prodávat a vracet produkty mimo sortiment obchodu. Stejně tak mohou zaměstnanci vyhledávat zákazníky, kteří jsou ve společnosti spojeni s běžným obchodem nebo jiným obchodem. Kromě toho mohou zaměstnanci vyhledávat zákazníky, kteří jsou spojeni s jinou společností v nadřazené organizaci.

## <a name="product-search"></a>Hledání produktu

Ve výchozím nastavení se vyhledávání produktů provádí v sortimentu obchodu. Tento typ vyhledávání se nazývá *vyhledávání místních produktů*. Zaměstnanci však mohou snadno přepnout do libovolného katalogu, který je přidružen k aktuálnímu obchodu, nebo mohou vyhledávat v jiném obchodě. Tento typ vyhledávání se nazývá *vyhledávání vzdálených produktů*. Chcete-li změnit katalog, zvolte tlačítko **Kategorie** v levé části stránky. V horní části zobrazeného podokna vyberte tlačítko **Změnit katalog** a vyberte jeden z dostupných katalogů pro jeho prohlížení. Systém bude prohledávat vybraný katalog produktů.

Na stránce **Změnit katalog** mohou zaměstnanci snadno vybrat libovolný obchod, nebo mohou vyhledávat produkty ve všech obchodech.

![Změna katalogu](./media/Changecatalog.png "Změna katalogu")

Vyhledávání místních produktů vyhledává v rámci následujících vlastností produktu:

- Číslo produktu
- Název produktu
- popis
- Dimenze
- Čárový kód
- Vyhledávací název

### <a name="enhancements-to-local-product-searches"></a>Vylepšení vyhledávání místních produktů

Zkušenosti při hledání místních produktů jsou uživatelsky přívětivější. Byla provedena následující vylepšení:

- Rozbalovací nabídky produktu a zákazníka byly přidány do vyhledávacího panelu, takže zaměstnanci mohou před vyhledáváním vybrat buď **Produkt** nebo **Zákazník**. Ve výchozím nastavení je vybrán **Produkt**, jak je uvedeno na následujícím obrázku.
- U vyhledávání s více klíčovými slovy (to znamená u vyhledávání, které používají hledané termíny) mohou prodejci nakonfigurovat, zda výsledky vyhledávání mají obsahovat výsledky, které odpovídají *libovolnému* hledanému termínu, nebo pouze výsledky, které odpovídají *všem* hledaným termínům. Nastavení této funkce je k dispozici v profilu funkce POS pod novou skupinou s názvem **Vyhledávání produktu**. Ve výchozím nastavení je **Spárovat jakékoli hledané termíny**. Toto nastavení je rovněž doporučené nastavení. Pokud je použito nastavení **Spárovat jakýkoli zadaný termín**, jsou vráceny všechny produkty, které plně nebo částečně odpovídají jednomu nebo více hledaným termínům. Výsledky se automaticky seřadí vzestupně podle produktů, které mají nejvíce shod klíčových slov (úplných nebo částečných).

    Nastavení **Spárovat všechny hledané termíny** vrátí pouze produkty odpovídající všem hledaným termínům (úplné nebo částečné). Toto nastavení je užitečné, když jsou názvy produktu dlouhé a zaměstnanci potřebují zobrazit pouze omezené produkty ve výsledcích vyhledávání. Tento typ vyhledávání však má dvě omezení:

    - Hledání se provádí na základě jednotlivých vlastností produktu. Jsou například vráceny pouze produkty, které mají všechna vyhledaná klíčová slova v alespoň jedné vlastnosti produktu.
    - Neprohledávají se dimenze.

- Maloobchodníci mohou nyní nakonfigurovat vyhledávání produktů pro zobrazení návrhů vyhledávání, když uživatelé zadávají názvy produktů. Nové nastavení této funkce je k dispozici v profilu funkce POS pod skupinu s názvem **Vyhledávání produktu**. Toto nastavení se nazývá **Zobrazit návrhy vyhledávání při zadávání**. Tato funkce pomůže zaměstnancům rychle najít produkt, který hledají, protože nemusí ručně zadávat celé jméno.
- Algoritmus vyhledávání produktu nyní hledá vyhledávané termíny ve vlastnosti produktu **Vyhledávání jména**.

![Návrhy produktů](./media/Productsuggestions.png "Návrhy produktů")

## <a name="customer-search"></a>Hledání zákazníka

Vyhledávání zákazníka slouží k vyhledání zákazníků pro různé účely. Pokladníci například mohou chtít zobrazit seznam přání zákazníka nebo historii nákupů, nebo přidat zákazníka do transakce. Vyhledávací algoritmus spáruje hledané termíny oproti hodnotám uvedeným v následujících vlastnostech odběratele:

- Název
- E-mailová adresa
- Telefonní číslo
- Číslo věrnostní karty
- Adresa
- Číslo účtu

V rámci těchto vlastností poskytuje název nejvyšší flexibilitu pro vyhledávání s více klíčovými slovy, protože algoritmus vrací všechny odběratele, kteří odpovídají jakémukoliv z hledaných klíčových slov. V horní části výsledků se objevují zákazníci, kteří odpovídají většině klíčových slov. Toto chování pomáhá pokladníkům v situacích, kdy hledají zadáním celého jména, ale příjmení a křestní jméno byly při původním zadání zaměněna. Z důvodu výkonu však všechny ostatní vlastnosti zachovávají pořadí klíčových slov pro vyhledávání. Pokud se tedy pořadí klíčových slov pro vyhledávání neshoduje s pořadím, ve kterém jsou data uložena, nebudou vráceny žádné výsledky.

Ve výchozím nastavení se vyhledávání zákazníků provádí na adresářích zákazníků, které jsou přiřazeny k obchodu. Tento typ vyhledávání se nazývá *vyhledávání místních zákazníků*. Zaměstnanci však mohou také vyhledávat zákazníky globálně. Jinými slovy, mohou vyhledávat ve všech obchodech společnosti a ve všech ostatních právnických osobách. Tento typ vyhledávání se nazývá *vyhledávání vzdálených zákazníků*.

Pokud chtějí vyhledávat globálně, mohou zaměstnanci vybrat tlačítko **Filtrovat výsledky** v dolní části stránky a potom vybrat možnost **Prohledat všechny obchody**, jak je znázorněno na následujícím obrázku. V takovém případě nejsou vráceni jen zákazníci. Všechny typy stran, které jsou součástí jakéhokoli adresáře v ústředí jsou vráceny též. Tyto strany zahrnují pracovníky, dodavatele, kontakty a konkurenty.

> [!NOTE]
> Aby bylo možné získat výsledky vyhledávání pro vzdáleného zákazníka, je třeba zadat minimálně čtyři znaky.

V případě vyhledávání vzdáleného zákazníka se ID zákazníka nezobrazuje pro zákazníky z jiných právnických osob, protože pro tyto strany v současné společnosti nebylo vytvořeno žádné ID zákazníka. Pokud však zaměstnanec otevře stránku s podrobnostmi o zákazníkovi, systém automaticky vygeneruje ID zákazníka pro danou stranu a zároveň propojí adresáře zákazníka obchodu se zákazníkem. Proto bude zákazník viditelný v prohledáváních místního obchodu, která budou provedena později.

![Globální vyhledávání zákazníků](./media/Globalcustomersearch.png "Globální vyhledávání zákazníků")

### <a name="enhancements-to-local-customer-search"></a>Vylepšení vyhledávání místních zákazníků

Hledání, které jsou založeny na telefonním čísle, byla zjednodušena. Tato hledání nyní ignorují speciální znaky, například mezery, pomlčky nebo hranaté závorky, které mohly být přidané při vytvoření odběratele. Pokladníci si tak nemusí dělat starosti s formátem telefonního čísla při hledání. Pokud telefonní číslo zákazníka byl zadáno například jako **123-456-7890**, pokladník můžete hledat zákazníka zadáním **1234567890**, nebo zadáním několika počátečních čísel telefonního čísla.

> [!NOTE]
> Zákazník může mít více telefonních čísel a více e-mailů. Algoritmus vyhledávání zákazníků také prochází těmito sekundárními e-maily a telefonními čísly, ale stránka s výsledky vyhledávání zákazníků zobrazuje pouze primární e-mail a telefonní číslo. To může způsobit určitý zmatek, protože vrácené výsledky zákazníka nezobrazí hledaný e-mail nebo telefonní číslo. V příštím vydání plánujeme vylepšit obrazovku výsledků vyhledávání zákazníků tak, aby se tyto informace zobrazovaly.

Tradiční vyhledávání zákazníků může být časově náročné, protože vyhledává mezi více poli. Místo toho mohou pokladníci nyní hledat v jedné vlastnosti zákazníka, jako je jméno, e-mailová adresa nebo telefonní číslo. Vlastnosti, které používá algoritmus hledání odběratele, jsou souhrnně označovány jako *kritéria hledání odběratele*. Správce systému může snadno konfigurovat jedno nebo více kritérií jako zástupce, který se zobrazí v POS. Vzhledem k tomu, že je hledání omezeno na jediné kritérium, jsou zobrazeny pouze relevantní výsledky hledání a výkon je mnohem lepší než výkon standardního hledání odběratele. Následující obrázek znázorňuje zkratky hledání odběratele v POS.

![Klávesové zkratky vyhledávání zákazníků](./media/SearchShortcutsPOS.png "Klávesové zkratky vyhledávání zákazníků")

Aby bylo možné nastavit kritérium hledání jako zástupce, musí správce otevřít stránku **Parametry Commerce** v aplikaci Commerce a poté na kartě **Kritéria vyhledávání POS** vybrat všechna kritéria, která se mají zobrazit jako zástupci.

![Konfigurovat klávesové zkratky vyhledávání](./media/ConfigureShortcutsAX.png "Konfigurovat zástupce vyhledávání")

> [!NOTE]
> Pokud přidáte příliš mnoho zástupců, rozevírací nabídka panelu vyhledávání v POS se přehltí a může to ovlivnit vyhledávání zaměstnance. Doporučujeme přidávat pouze tolik zástupců, kolik potřebujete.

Pole **Pořadí zobrazení** určuje pořadí, ve kterém jsou zobrazeny zkratky v POS. Kritéria, která jsou zobrazena ve vlastnostech ihned po vybalení, které používá algoritmus hledání odběratele pro hledání odběratele. Partneři však mohou přidat vlastní vlastnosti jako zástupce hledání. Pokud chcete přidat vlastní vlastnosti jako zkratky hledání, musí správce systému rozšířit rozšiřitelné vyčíslení (enum), které se používá pro kritéria vyhledávání odběratele, a následně označit vlastní vlastnosti partnera jako zástupce. Partneři zodpovídají za zápis kódu k vyhledání výsledků, když se používají k hledání jejich vlastní zástupci.

> [!NOTE]
> Vlastní vlastnost, která je přidána do výčtu, neovlivní standardní algoritmus hledání odběratele. Jinými slovy, algoritmus hledání zákazníků nevyhledává ve vlastní vlastnosti. Uživatelé mohou vlastní vlastnosti použít k vyhledávání pouze v případě, že je vlastní vlastnost přidána jako zástupce, případně je přepsán výchozí algoritmus hledání.

V nadcházející verzi aplikace Commerce budou maloobchodní prodejci moci nastavit výchozí režim vyhledávání odběratelů v aplikaci POS pro možnost **Prohledat všechny obchody**. Tato konfigurace může být užitečná ve scénářích, ve kterých je nutné, aby zákazníci, kteří byli vytvořeni mimo POS, byli vyhledání okamžitě (například před spuštěním úlohy distribuce). Ve funkčním profilu POS bude k dispozici nová možnost **Výchozí režim vyhledávání odběratelů**. Nastavením této možnosti na **Zapnuto** nastavíte výchozí režim vyhledávání pro možnost **Prohledat všechny obchody**. Každý pokus o hledání odběratele poté provede volání do centrály v reálném čase.

Aby se zabránilo neočekávaným problémům s výkonem, je tato konfigurace skryta za testovacím příznakem s názvem **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING**. Chcete-li tedy zobrazit možnost **Výchozí režim vyhledávání odběratelů** nastavující uživatelské rozhraní (UI), měl by maloobchodní prodejce vytvořit lístek podpory pro akceptační testování uživatele a výrobní prostředí. Po obdržení lístku bude tým inženýrů spolupracovat s maloobchodním prodejcem, aby se ujistil, že prodejce provádí testování v nevýrobním prostředí, aby zhodnotil výkonnost a implementoval požadované optimalizace.



[!INCLUDE[footer-include](../includes/footer-banner.md)]