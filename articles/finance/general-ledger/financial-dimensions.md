---
title: Finanční dimenze
description: Tento článek popisuje různé typy finančních dimenzí a způsob jejich nastavení.
author: aprilolson
ms.date: 03/07/2022
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 3ad92e006351adbf2494a1b32325d2d4a83b76a4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849982"
---
# <a name="financial-dimensions"></a>Finanční dimenze

[!include [banner](../includes/banner.md)]

Tento článek popisuje různé typy finančních dimenzí a způsob jejich nastavení.

Pomocí stránky **Finanční dimenze** můžete vytvářet finanční dimenze, které lze použít jako segmenty účtu pro účtové osnovy. Existují dva typy finančních dimenzí – vlastní dimenze a dimenze zajištěné entitou. Vlastní dimenze jsou společné pro více právnických osob a jejich hodnoty zadávají a spravují uživatelé. U dimenzí zajištěných entitou jsou hodnoty definovány jinde v systému, například v entitách Odběratelé nebo Obchody. Některé dimenze zajištěné entitami jsou společné pro více právnických osob, zatímco jiné platí pro konkrétní společnost.

Po vytvoření finančních dimenzí použijte stránku **Hodnoty finanční dimenze** k přiřazení dalších vlastností ke každé finanční dimenzi.

Finanční dimenze mohou reprezentovat právnické osoby. Není nutné vytvářet právnické osoby v Dynamics 365 Finance. Finanční dimenze však nejsou určeny k řešení provozních nebo obchodních požadavků právnických osob. Funkce mezijednotkového účetnictví ve Finance umožňuje pracovat pouze s účetními položkami vytvořenými jednotlivými transakcemi.

Než nastavíte finanční dimenze jako právnické osoby, vyhodnoťte obchodní procesy v následujících oblastech a určete, zda bude tento systém ve vaší organizaci fungovat:

- Zásoby
- Nákup a prodej mezi finančními dimenzemi a právnickými osobami
- Výpočet a vykazování DPH
- Operační vykazování

Zde jsou uvedena některá omezení:

- Funkci DPH lze používat pouze s právnickými osobami, ale ne s finančními dimenzemi.
- Některé sestavy neobsahují finanční dimenze. Pokud tedy budete chtít tyto dimenze v sestavách použít, bude možná nutné sestavy upravit.

## <a name="custom-dimensions"></a>Vlastní dimenze

Pokud chcete vytvořit hodnoty definované uživatelem, vyberte v poli **Použít hodnoty z** možnost **Vlastní dimenze**.

Můžete také učit účetní masku pro omezení množství a typů informací, které lze zadat pro hodnoty dimenze. Můžete zadat znaky, které zůstanou u všech hodnot dimenze stejné, například písmena nebo spojovníky (-). Můžete také zadat znaky čísel (\#) a znak ampersand (&) jako zástupné symboly pro znaky, která se změní pokaždé, když je hodnota dimenze vytvořena. Použijte znak čísla (\#) jako zástupný symbol pro číslo a ampersand (&) jako zástupný symbol pro písmeno. Pole masky formátu je k dispozici pouze tehdy, pokud vyberete možnost **Vlastní dimenze** v poli **Použít hodnoty od**.

**Příklad**

Chcete-li omezit hodnotu dimenze na písmena „CC“ a tři čísla, zadejte jako masku formátu **CC-\#\#\#**.

## <a name="entity-backed-dimensions"></a>Dimenze zajištěné entitou

Pokud chcete použít finanční dimenzi zajištěnou entitou, vyberte v poli **Použít hodnoty od** systémem definovanou entitu, která bude základem dimenze. Hodnoty finanční dimenze se vytvoří z této entity. Chcete-li například vytvořit hodnoty dimenze pro projekty, vyberte možnost **Projekty**. Hodnota dimenze se vytvoří pro každý název projektu. Stránka **Hodnoty finanční dimenze** uvádí hodnoty pro entitu. Pokud tyto hodnoty platí pro konkrétní společnost, zobrazí se i její název.

## <a name="activating-dimensions"></a>Aktivační dimenze

Při aktivaci finanční dimenze se tabulka aktualizuje a zobrazí se v ní název dimenze. Odstraněné dimenze budou odebrány. Před aktivací finanční dimenze můžete zadat hodnoty dimenze. Finanční dimenze lze však upotřebit až po aktivaci. Například nelze přidat finanční dimenzi do účetní struktury, dokud ji neaktivujete. Po zvolení možnosti **Aktivovat** se všechny dimenze aktualizují a zobrazí se změny stavu.

## <a name="translations"></a>Překlady

Na stránce **Překlad textu** můžete zadat text vybrané finanční dimenze v různých jazycích. Na stránce **Překlad hlavního účtu** můžete zadat text hlavního účtu v různých jazycích. 

## <a name="legal-entity-overrides"></a>Přepisy právnických osob

Ne všechny dimenze jsou u všech právnických osob platné. Některé dimenze kromě toho mohou platit jen v určitém období. V takových případech lze pomocí části **Přepisy právnických osob** určit společnosti, u kterých má být použití dimenze pozastaveno, kdo je vlastníkem a období aktivity dimenze.

## <a name="deleting-financial-dimensions"></a>Odstranění finančních dimenzí

V zájmu udržení referenční integrity dat lze finanční dimenze v řídkých případech odstranit. Při pokusu o odstranění finanční dimenze jsou vyhodnocena následující kritéria:

- Byla finanční dimenze použita pro zaúčtované a nezaúčtované transakce nebo v jakémkoli typu kombinace hodnot dimenzí?
- Používá se finanční dimenze v nějaké aktivní účetní struktuře, struktuře rozšířeného pravidla nebo sadě finančních dimenzí?
- Je finanční dimenze součástí výchozího formátu integrace finanční dimenze?
- Byla finanční dimenze nastavena jako výchozí dimenze?
- Byla v nastavení Financial Reporting zrušena volba finanční dimenze? 

Pokud je odpověď na některou z těchto otázek kladná, finanční dimenzi nelze odstranit.

> [!NOTE]
> Počínaje verzí Finance 10.0.27 již nebudou finanční dimenze automaticky vybírány pro nastavení finančního výkaznictví při jejich vytváření. 

## <a name="default-dimension-values"></a>Výchozí hodnoty dimenze

Můžete použít hodnoty z hlavních záznamů, jako například odběratele a dodavatele, jako výchozí hodnoty v nových dimenzích. Při vytvoření nových dimenzí se zadá do hodnot dimenzí těchto hlavních záznamů ID hlavního záznamu. Například při vytváření nového odběratele se zadá do dimenze odběratele ID odběratele. Při vytváření prodejních objednávek, faktur nebo jiných dokumentů, které vyžadují ID odběratele, se použijí existující výchozí pravidla, a do dokumentu se přidá ID odběratele.

Tato funkce je řízena nastavením v dimenzi. Toto nastavení se jmenuje **Kopírování hodnot do této dimenze na každé nové vytvořené DimensionName**, kde **DimensionName** je název dimenze. Ve výchozím nastavení je tato funkce vypnutá. Lze ji však kdykoliv zapnout.

Pokud pro dimenzi již existují záznamy, hlavní záznamy se aktualizují, když zapnete funkci. Stávající dokumenty a transakce však nebudou aktualizovány.

Pokud použijete šablonu pro vytvoření hlavního záznamu, ujistěte se, že hodnota šablony základní dimenze není vyplněná. Pokud například vytváříte odběratele ze šablony, ujistěte se, že je dimenze odběratele v šabloně prázdná. Hodnota dimenze pro odběratele bude přednastavena z nového čísla zákazníka při vytvoření nového odběratele.  

## <a name="derived-dimensions"></a>Odvozené dimenze

Dimenze lze nakonfigurovat tak, aby se informace pro jiné dimenze automaticky zadaly, když zadáte tuto dimenzi do dokumentu. Pokud zadáte nákladové středisko 10, hodnotu **20** lze automaticky zadat do dimenze oddělení.

Můžete nastavit odvozené hodnoty na stránce dimenzí.

1. Vyberte dimenzi a poté vyberte **Odvozené dimenze**.

    Stránka **Odvozené dimenze** obsahuje mřížku. Vybraný segment dimenze je první sloupec v této mřížce.

2. Přidejte segmenty, které by měly být odvozeny. Každý segment se zobrazí jako sloupec.

Zadejte kombinace dimenzí, které by měly být odvozeny od dimenze v prvním sloupci. Například chcete-li použít nákladové středisko jako dimenzi, ze které je odvozené oddělení a místo, zadejte nákladové středisko 10, oddělení 20 a skladové místo 30. Poté když zadáte v hlavním záznamu nebo na stránce transakce nákladové středisko 10, oddělení 20 a místo 30 se zadají automaticky.

### <a name="overriding-existing-values-with-derived-dimensions"></a>Přepsání stávajících hodnot odvozenými dimenzemi
 
Ve výchozím nastavení proces odvozené dimenze nepřepíše existující hodnoty pro odvozené dimenze. Například pokud zadáte nákladové středisko 10 a žádnou další dimenzi, jsou ve výchozím nastavení zadány oddělení 20 a místo 30. Změníte-li však nákladové středisko, již zřízené hodnoty se nezmění. Proto je možné vytvořit výchozí dimenze na hlavních záznamech a tyto dimenze se nezmění odvozenými dimenzemi.

Můžete změnit chování odvozených dimenzí pro přepsání stávajících hodnot výběrem zaškrtávacího políčka **Nahradit stávající hodnoty dimenze odvozený hodnotami** na stránce **Odvozené dimenze**. Je-li toto políčko zaškrtnuto, můžete zadat dimenzi s hodnotami odvozené dimenze a tyto hodnoty odvozené dimenze přepíšou hodnoty, které již existují. V předchozím příkladu, pokud zadáte nákladové středisko 10 a žádnou další dimenzi, jsou ve výchozím nastavení zadány oddělení 20 a místo 30. Pokud však hodnoty byly již oddělení 50 a místo 60, nyní se změní hodnoty na oddělení 20 a místo 30.
 
Odvozené dimenze s tímto nastavením automaticky nenahradí existující výchozí hodnoty dimenze, když jsou hodnoty dimenzí ve výchozím nastavení. Hodnoty dimenze budou přepsány pouze tehdy, pokud zadáte novou hodnotu dimenze na stránce a pokud existují odvozené hodnoty pro tuto dimenzi na této stránce.

### <a name="preventing-changes-with-derived-dimensions"></a>Zabránění změnám s odvozenými dimenzemi
 
Pokud používáte **Přidat segment "** na stránce **Odvozené dimenze** pro přidání segmentu jako odvozené dimenze, máte k dispozici možnost v dolní části stránky **Přidat segment**, která umožňuje zabránit změnám dimenze, když je na stránce odvozena. Ve výchozím nastavení je vypnutá, aby nebránila změnám hodnot odvozené dimenze. Změňte nastavení na **Ano**, pokud chcete zabránit změně dimenze poté, co byla odvozena. Například pokud je hodnota dimenze Oddělení odvozena z hodnoty dimenze nákladového střediska, nelze hodnotu oddělení změnit, pokud je možnost **Zabránit změnám** nastavena na **Ano**. 
 
Nastavení nebrání změnám, pokud je hodnota dimenze platná, ale není uvedena v seznamu odvozených dimenzí. Například pokud je oddělení 20 odvozeno z nákladového střediska 10 a vy zadáte nákladové středisko 10, nebude pak možné upravit oddělení 20. Avšak pokud zadáte nákladové středisko 20 a to se nenachází v seznamu odvozených dimenzí pro nákladové středisko, můžete pak upravit hodnotu oddělení. 
 
Ve všech případech hodnota účtu a hodnoty všech dimenzí budou stále ověřovány proti účetním strukturám po použití hodnot odvozených dimenzí. Pokud používáte odvozené dimenze a jejich ověření při použití na stránce se nezdaří, musíte změnit hodnoty odvozené dimenze na stránce odvozených dimenzí, než je bude možné použít v transakcích. 
 
Pokud změníte dimenze na pevné záložce **Finanční dimenze**, dimenzi, která je označena k zabránění změnám, nebude možné upravovat. Pokud zadáváte účet a dimenze do ovládacího prvku segmentovaného zadávání na stránce, lze dimenze upravit. Avšak při přesunutí zvýraznění z ovládacího prvku segmentovaného zadávání a přesunutí do jiného pole nebo provedení akce budou účet a dimenze ověřeny proti seznamu odvozených dimenzí a účetních struktur, aby bylo zajištěno, že jste zadali příslušné hodnoty. 

### <a name="derived-dimensions-and-entities"></a>Odvozené dimenze a entity

Segmenty odvozených dimenzí a hodnoty můžete nastavit pomocí entit.

- Entita odvozených dimenzí nastavuje řídicí dimenze a segmenty, které se používají pro tyto dimenze.
- Entita hodnoty odvozených dimenzí umožňuje importovat hodnoty, které by měly být odvozeny pro každou řídicí dimenzi.

Při použití entitu pro import dat, pokud entita importuje dimenze, se použijí pravidla odvozené dimenze během importu, pokud entita konkrétně nepřepíše tyto dimenze.

Další informace naleznete v následujících tématech:

- [Definování finančních dimenzí](tasks/define-financial-dimensions.md)
- [Udržování výchozích šablon finančních dimenzí](tasks/maintain-financial-dimension-default-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
