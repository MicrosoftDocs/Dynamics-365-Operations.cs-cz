---
title: "Finanční dimenze"
description: "Toto téma popisuje různé typy finančních dimenzí a způsob jejich nastavení."
author: aprilolson
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: d6b7b1219974cb5de1a625d87c3bce2a4439470b
ms.openlocfilehash: 9973d03de031ad2fa5647bb167c12b9231633a22
ms.contentlocale: cs-cz
ms.lasthandoff: 10/01/2018

---

# <a name="financial-dimensions"></a>Finanční dimenze

[!include [banner](../includes/banner.md)]

Toto téma popisuje různé typy finančních dimenzí a způsob jejich nastavení.

Pomocí stránky **Finanční dimenze** můžete vytvářet finanční dimenze, které lze použít jako segmenty účtu pro účtové osnovy. Existují dva typy finančních dimenzí – vlastní dimenze a dimenze zajištěné entitou. Vlastní dimenze jsou společné pro více právnických osob a jejich hodnoty zadávají a spravují uživatelé. U dimenzí zajištěných entitou jsou hodnoty definovány jinde v systému, například v entitách Odběratelé nebo Obchody. Některé dimenze zajištěné entitami jsou společné pro více právnických osob, zatímco jiné platí pro konkrétní společnost.

Po vytvoření finančních dimenzí použijte stránku **Hodnoty finanční dimenze** k přiřazení dalších vlastností ke každé finanční dimenzi.

Finanční dimenze mohou reprezentovat právnické osoby. V aplikaci Microsoft Dynamics 365 for Finance and Operations nemusíte právnické osoby vytvářet. Finanční dimenze však nejsou určeny k řešení provozních nebo obchodních požadavků právnických osob. Funkce mezijednotkového účetnictví v aplikaci Finance and Operations je určena pouze k práci s účetními položkami vytvořenými jednotlivými transakcemi.

Než nastavíte finanční dimenze jako právnické osoby, vyhodnoťte obchodní procesy v následujících oblastech a určete, zda bude tento systém ve vaší organizaci fungovat:

- Zásoby
- Nákup a prodej mezi finančními dimenzemi a právnickými osobami
- Výpočet a vykazování DPH
- Operační vykazování

Zde jsou uvedena některá omezení:

- Funkci DPH lze používat pouze s právnickými osobami, ale ne s finančními dimenzemi.
- Některé sestavy neobsahují finanční dimenze. Pokud tedy budete chtít tyto dimenze v sestavách použít, bude možná nutné sestavy upravit.

## <a name="custom-dimensions"></a>Vlastní dimenze

Pokud chcete vytvořit hodnoty definované uživatelem, vyberte v poli **Použít hodnoty od** možnost **&lt;&nbsp;Vlastní dimenze&nbsp;&gt;**.

Můžete také učit účetní masku pro omezení množství a typů informací, které lze zadat pro hodnoty dimenze. Můžete zadat znaky, které zůstanou u všech hodnot dimenze stejné, například písmena nebo spojovníky (-). Můžete také zadat znaky čísel (\#) a znak ampersand (&) jako zástupné symboly pro znaky, která se změní pokaždé, když je hodnota dimenze vytvořena. Použijte znak čísla (\#) jako zástupný symbol pro číslo a ampersand (&) jako zástupný symbol pro písmeno. Pole masky formátu je k dispozici pouze tehdy, pokud vyberete možnost **&lt;&nbsp;Vlastní dimenze&nbsp;&gt;** v poli **Použít hodnoty od**.

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

Pokud je odpověď na některou z těchto otázek kladná, finanční dimenzi nelze odstranit.

## <a name="default-dimension-values"></a>Výchozí hodnoty dimenze

Můžete použít hodnoty z hlavních záznamů, jako například odběratele a dodavatele, jako výchozí hodnoty v nových dimenzích. Při vytvoření nových dimenzí se zadá do hodnot dimenzí těchto hlavních záznamů ID hlavního záznamu. Například při vytváření nového odběratele se zadá do dimenze odběratele ID odběratele. Při vytváření prodejních objednávek, faktur nebo jiných dokumentů, které vyžadují ID odběratele, se použijí existující výchozí pravidla, a do dokumentu se přidá ID odběratele.

Tato funkce je řízena nastavením v dimenzi. Toto nastavení se jmenuje **Kopírování hodnot do této dimenze na každé nové vytvořené DimensionName**, kde **DimensionName** je název dimenze. Ve výchozím nastavení je tato funkce vypnutá. Lze ji však kdykoliv zapnout.

Pokud pro dimenzi již existují záznamy, hlavní záznamy se aktualizují, když zapnete funkci. Stávající dokumenty a transakce však nebudou aktualizovány.

## <a name="derived-dimensions"></a>Odvozené dimenze

Dimenze lze nakonfigurovat tak, aby se informace pro jiné dimenze automaticky zadaly, když zadáte tuto dimenzi do dokumentu. Pokud zadáte nákladové středisko 10, hodnotu **20** lze automaticky zadat do dimenze oddělení.

Můžete nastavit odvozené hodnoty na stránce dimenzí.

1. Vyberte dimenzi a poté vyberte **Odvozené dimenze**.

    Stránka **Odvozené dimenze** obsahuje mřížku. Vybraný segment dimenze je první sloupec v této mřížce.

2. Přidejte segmenty, které by měly být odvozeny. Každý segment se zobrazí jako sloupec.

Zadejte kombinace dimenzí, které by měly být odvozeny od dimenze v prvním sloupci. Například chcete-li použít nákladové středisko jako dimenzi, ze které je odvozené oddělení a místo, zadejte nákladové středisko 10, oddělení 20 a skladové místo 30. Poté když zadáte v hlavním záznamu nebo na stránce transakce nákladové středisko 10, oddělení 20 a místo 30 se zadají automaticky.

Proces odvozené dimenze nepřepíše existující hodnoty pro odvozené dimenze. Například pokud zadáte nákladové středisko 10 a žádnou další dimenzi, jsou ve výchozím nastavení zadány oddělení 20 a místo 30. Změníte-li však nákladové středisko, již zřízené hodnoty se nezmění. Proto je možné vytvořit výchozí dimenze na hlavních záznamech a tyto dimenze se nezmění odvozenými dimenzemi.

### <a name="derived-dimensions-and-entities"></a>Odvozené dimenze a entity

Segmenty odvozených dimenzí a hodnoty můžete nastavit pomocí entit.

- Entita odvozených dimenzí nastavuje řídicí dimenze a segmenty, které se používají pro tyto dimenze.
- Entita DerivedDimensionValue umožňuje importovat hodnoty, které by měly být odvozeny pro každou řídicí dimenzi.

Při použití entitu pro import dat, pokud entita importuje dimenze, se použijí pravidla odvozené dimenze během importu, pokud entita konkrétně nepřepíše tyto dimenze.

Další informace naleznete v následujících tématech:

- [Definování finančních dimenzí](tasks/define-financial-dimensions.md)
- [Udržování výchozích šablon finančních dimenzí](tasks/maintain-financial-dimension-default-templates.md)

