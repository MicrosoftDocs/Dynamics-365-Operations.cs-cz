---
title: Technické atributy a vyhledávání technických atributů
description: Toto téma vysvětluje, jak můžete pomocí technických atributů určit všechny nestandardní vlastnosti, abyste zajistili, že v systému budou zaregistrována všechna kmenová data produktu. Vysvětluje také, jak můžete pomocí vyhledávání technických atributů snadno najít produkty na základě těchto registrovaných vlastností.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 5cb4c2b9b4a3c54e71f73369096d00b436079c1c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475005"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a>Technické atributy a vyhledávání technických atributů

[!include [banner](../includes/banner.md)]

K zajištění, jak lze v systému registrovat hlavní data produktu, můžete pomocí technických atributů určit všechny nestandardní vlastnosti. Následně můžete pomocí vyhledávání technických atributů snadno najít produkty na základě těchto registrovaných vlastností.

## <a name="create-engineering-attributes-and-attribute-types"></a>Vytvoření technických atributů a typů atributů

Strojírenské produkty mají obvykle mnoho charakteristik a vlastností, které musíte zachytit. Ačkoli můžete zaregistrovat některé vlastnosti pomocí standardních polí produktu, můžete podle potřeby vytvořit také nové technické vlastnosti. Můžete definovat vlastní *technické atributy* a nastavit je jako součást definice produktu.

Každý technický atribut musí patřit k *typu atributu*. Tento požadavek existuje, protože každý technický atribut musí mít *datový typ*, který definuje typy hodnot, které může obsahovat. Typ technického atributu může být standardní typ (například volný text, celé číslo nebo desetinné číslo) nebo vlastní typ (například text, který má na výběr konkrétní sadu hodnot). Každý typ atributu můžete znovu použít s libovolným počtem technických atributů.

### <a name="set-up-engineering-attribute-types"></a>Nastavení typů technických atributů

Chcete-li zobrazit, vytvořit nebo upravit typ technického atributu, postupujte takto.

1. Jděte na **Správa technických změn \> Nastavení \> Atributy \> Typy atributů**.
1. Vyberte existující atribut v podokně seznamu nebo vyberte **Nový** v podokně akcí a vytvořte nový typ atributu.
1. Nastavte následující pole:

    - **Název typu atributu** – zadejte název typu atributu.
    - **Typ** - Vyberte standardní datový typ (*Měna*, *Čas schůzky*, *Desetinný*, *Celé číslo*, *Text*, *Logický* nebo *Odkaz*).
    - **Opravený seznam** - Tato možnost je k dispozici, pouze pokud nastavíte pole **Typ** na *Text*. Nastavte ho na *Ano*, pokud chcete definovat konkrétní hodnoty pro atributy tohoto typu. V tomto případě bude vytvořen rozevírací seznam. Používáte pevnou záložku **Hodnota** k určení hodnot, které jsou k dispozici pro tento typ atributu. Tuto možnost nastavte na *Ne*, abyste uživatelům umožnili zadat libovolnou hodnotu. V takovém případě bude vytvořeno vstupní pole.
    - **Rozsah hodnot** - Tato možnost je k dispozici, pouze pokud nastavíte pole **Typ** na *Celé číslo*, *Desetinný* nebo *Měna*. Nastavte ji na *Ano*, pokud chcete stanovit minimální a maximální hodnoty, které budou přijaty pro atributy tohoto typu. Používáte pevnou záložku **Rozsah** ke stanovení minimální a maximální hodnoty a (pro měnu) měny, která platí pro limity, které jste zadali. Tuto možnost nastavte na *Ne*, abyste mohli přijmout jakoukoli hodnotu. 
    - **Měrná jednotka** – Toto pole je dostupné, pouze pokud nastavíte pole **Typ** na *Celé číslo* nebo *Desetinná hodnota*. Vyberte měrnou jednotku, která platí pro tento typ atributu. Pokud není vyžadována žádná jednotka, ponechte toto pole prázdné.

### <a name="set-up-engineering-attributes"></a>Nastavení technických atributů

Chcete-li zobrazit, vytvořit nebo upravit technický atribut, postupujte takto.

1. Jděte na **Správa technických změn \> Nastavení \> Atributy \> Technické atributy**.
1. Vyberte existující atribut v podokně seznamu nebo vyberte **Nový** v podokně akcí a vytvořte nový atribut.
1. Nastavte následující pole:

    - **Název** - Zadejte název atributu. Tento název se zobrazuje pouze na stránce **Technické atributy**. Na každém jiném místě systému se obvykle zobrazuje hodnota pole **Popisný název** k určení atributu.
    - **Typ atributu** - Vyberte typ atributu, který jste definovali v předchozí části.
    - **Popisný název** - Zadejte název, který identifikuje atribut v systému (s výjimkou stránky **Technické atributy**). 
    - **Popis** - zadejte popis atributu.
    - **Text nápovědy** - Zadejte text nápovědy, který řekne ostatním uživatelům, k čemu je atribut určen.
    - **Výchozí hodnota** - Zadejte výchozí hodnotu pro atribut. Zobrazené možnosti závisí na typu atributu, který jste vybrali.
    - **Měna** - Pokud je typ atributu, který jste vybrali, měna, vyberte měnu, kterou bude atribut akceptovat, a zobrazte hodnoty.

1. Pokud je typ atributu, který jste vybrali, celé číslo nebo desetinné číslo, zobrazí se pevná záložka **Rozsah**. Na této pevné záložce podle potřeby nastavte následující pole:

    - **Akce tolerance** - Vyberte, jak má systém reagovat, pokud uživatel zadá hodnotu mimo zadaný rozsah. Pokud vyberete *Varování*, zobrazí se varování, ale uživatel může hodnotu uložit. Pokud vyberete *Nepovoleno*, zobrazí se varování a hodnotu nelze uložit, dokud ji uživatel neopraví.
    - **Minimální** - Zadejte minimální doporučenou nebo akceptovanou hodnotu.
    - **Maximální** - Zadejte maximální doporučenou nebo akceptovanou hodnotu.

### <a name="engineering-attribute-inheritance"></a>Dědičnost technických atributů

U struktur produktů, jako jsou kusovníky (BOM) nebo vzorce, lze vybrané atributy předávat od podřízených položek až po nadřazené položky. Tento proces můžete považovat za „reverzní dědičnost“.

#### <a name="turn-on-this-feature-for-your-system"></a>Zapnutí této funkce ve vašem systému

Pokud váš systém ještě neobsahuje funkce popsané v této části, přejděte na stránku [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Plánované výrobní zakázky pomocí optimalizace plánování*.

#### <a name="attribute-inheritance-example"></a>Příklad dědičnosti atributů

U potravinářského výrobku, jako je mrkvový koláč, musí systém zaznamenat každý alergen, který výrobek obsahuje. Mrkvový dort lze v systému modelovat jako technický výrobek, který má vzorec. Tento vzorec obsahuje ingredience mrkvového koláče, jako je mouka, mléko, mrkev a ořechy. V tomto případě společnost poskytuje dva modely pro mrkvový dort: jeden, který obsahuje laktózu a druhý, který neobsahuje.

Dort, který obsahuje laktózu, má na úrovni přísad následující atributy:

- Ingredience „mouka“: atribut „lepek“ = ano
- Ingredience „mléko“: atribut „laktóza“ = ano
- Ingredience „ořechy“: atribut „ořechy“ = ano

Dort, který neobsahuje laktózu, používá mléko bez laktózy a má na úrovni ingrediencí následující atributy:

- Ingredience „mouka“: atribut „lepek“ = ano
- Ingredience „mléko“: atribut „laktóza“ = ne
- Ingredience „ořechy“: atribut „ořechy“ = ano

Protože jsou tyto produkty většinou podobné, mohlo by být vhodné předat tyto atributy z podřízených položek (dvě varianty) do nadřazeného produktu (základní mrkvový dort). K implementaci této „reverzní dědičnosti“ můžete použít funkci *Přiřadit dědičnost*. Tato funkce je definována pro každou [technickou verzi](engineering-versions-product-category.md).

## <a name="connect-engineering-attributes-to-an-engineering-product-category"></a>Připojte technické atributy ke kategorii strojírenských produktů

Některé technické atributy platí pro všechny produkty, zatímco jiné jsou specifické pro jednotlivé produkty nebo kategorie produktů. Například elektrické atributy nejsou pro mechanické výrobky vyžadovány. Proto můžete nastavit *kategorie technických výrobků*. Kategorie technického produktu zavádí soubor technických atributů, které musí být součástí definice produktů, které do této kategorie patří. Můžete také určit, které technické atributy jsou povinné a zda existuje výchozí hodnota.

Další informace o tom, jak pracovat s kategoriemi technických produktů, včetně informací o tom, jak připojit atributy ke kategoriím, najdete v části [Technické verze a kategorie technických produktů](engineering-versions-product-category.md).

## <a name="set-attribute-values-for-engineering-attributes"></a>Nastavení hodnot atributů pro technické atributy

Technické atributy, které jsou spojeny s kategorií technického produktu, se zobrazí, když vytvoříte nový technický produkt založený na dané kategorii. V té době můžete nastavit hodnoty pro atributy. Později lze tyto hodnoty změnit na stránce **Technická verze** nebo v rámci správy technických změn v pořadí technických změn. Další informace naleznete v tématu [Správa změn technických produktů](engineering-change-management.md).

## <a name="create-an-engineering-product"></a>Vytvoření technického produktu

Chcete-li vytvořit technický produkt, otevřete stránku **Vydané produkty**. Poté v podokně akcí na kartě **Produkt** ve skupině **Nový** zvolte **Technický produkt**.

Musíte určit technickou kategorii, do které produkt patří. Kategorie nastaví všechny výchozí hodnoty a vlastnosti produktu. Rovněž nastaví atributy, které se na produkt vztahují. Po výběru kategorie se nastaví hodnoty atributů. Tyto hodnoty pak můžete upravit.

## <a name="search-for-products-by-using-engineering-attribute-values"></a>Hledání produktů pomocí hodnot technických atributů

Můžete použít vyhledávání technických atributů k vyhledání produktů hledáním jejich hodnot technických atributů. Proto můžete snadno najít technické produkty na základě jejich vlastností. Můžete vyhledávat v produktech, které patří do kategorie technických produktů nebo prohledat všechny technické produkty.

Hledání je k dispozici na stránkách hlavních dat produktu a z transakčních položek v systému, například prodejních objednávek. U transakční položky můžete použít stránku **Hledání technických atributů** pro vyhledání produktu. Poté můžete použít tlačítko **Přidat jako nový řádek** pro přidání produktu na řádky prodejní objednávky. Produkty ve výsledcích vyhledávání lze také přidat přímo do objednávky.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
