---
title: "Finanční dimenze"
description: "Toto téma popisuje různé typy finančních dimenzí a způsob jejich nastavení."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: a0edbad63c51d111d7c8985aa7fdf7312da6149d
ms.openlocfilehash: e82d53b3f6b4c8d3e2363f26576331e1d03434d9
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017


---

# <a name="financial-dimensions"></a>Finanční dimenze

[!include[banner](../includes/banner.md)]

Toto téma popisuje různé typy finančních dimenzí a způsob jejich nastavení.

Pomocí stránky **Finanční dimenze** můžete vytvářet finanční dimenze, které lze použít jako segmenty účtu pro účtové osnovy. Existují dva typy finančních dimenzí – vlastní dimenze a dimenze zajištěné entitou. Vlastní dimenze jsou společné pro více právnických osob a jejich hodnoty zadávají a spravují uživatelé. U dimenzí zajištěných entitou jsou hodnoty definovány jinde v systému, například v entitách Odběratelé nebo Obchody. Některé dimenze zajištěné entitami jsou společné pro více právnických osob, zatímco jiné platí pro konkrétní společnost. 

Po vytvoření finančních dimenzí použijte stránku **Hodnoty finanční dimenze** k přiřazení dalších vlastností ke každé finanční dimenzi. 

Finanční dimenze mohou reprezentovat právnické osoby. V aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition nemusíte právnické osoby vytvářet. Finanční dimenze však nejsou určeny k řešení provozních nebo obchodních požadavků právnických osob. Funkce mezijednotkového účetnictví v aplikaci Finance and Operations je určena pouze k práci s účetními položkami vytvořenými jednotlivými transakcemi. 

Než nastavíte finanční dimenze jako právnické osoby, vyhodnoťte obchodní procesy v následujících oblastech a určete, zda bude tento systém ve vaší organizaci fungovat:

- Zásoby
- Nákup a prodej mezi finančními dimenzemi a právnickými osobami
- Výpočet a vykazování DPH
- Operační vykazování

Zde jsou uvedena některá omezení:

- Funkci DPH lze používat pouze s právnickými osobami, ale ne s finančními dimenzemi.
- Některé sestavy neobsahují finanční dimenze. Pokud tedy budete chtít tyto dimenze v sestavách použít, bude možná nutné sestavy upravit.

## <a name="custom-dimensions"></a>Vlastní dimenze

Pokud chcete vytvořit uživatelskou finanční dimenzi, vyberte v poli **Použít hodnoty od** možnost **&lt;Vlastní dimenze&gt;**. Můžete také učit účetní masku pro omezení množství a typů informací, které můžete zadat pro hodnoty dimenze. Můžete zadat znaky, které zůstanou u všech hodnot dimenze stejné, například písmena nebo spojovníky (-). Můžete také zadat znaky čísel (\#) a znak ampersand (&) jako zástupné symboly pro písmena a čísla, která se změní pokaždé, když je hodnota dimenze vytvořena. Použijte znak čísla (\#) jako zástupný symbol pro číslo a ampersand (&) jako zástupný symbol pro písmeno. Pole masky formátu je k dispozici pouze tehdy, pokud vyberete možnost **&lt;Vlastní dimenze&gt;** v poli **Použít hodnoty od**.

**Příklad**

Chcete-li omezit hodnotu dimenze na písmena „CC“ a tři čísla, zadejte jako masku formátu **CC-\#\#\#**.

## <a name="entity-backed-dimensions"></a>Dimenze zajištěné entitou

Pokud chcete použít finanční dimenzi zajištěnou entitou, vyberte v poli **Použít hodnoty od** systémem definovanou entitu, která bude základem dimenze. Hodnoty finanční dimenze se vytvoří z této entity. Chcete-li například vytvořit hodnoty dimenze pro projekty, vyberte možnost **Projekty**. Hodnota dimenze se vytvoří pro každý název projektu. Stránka **Hodnoty finanční dimenze** uvádí hodnoty pro entitu. Pokud tyto hodnoty platí pro konkrétní společnost, zobrazí se i její název.

## <a name="activating-dimensions"></a>Aktivační dimenze

Při aktivaci finanční dimenze se tabulka aktualizuje a zobrazí se v ní název dimenze. Odstraněné dimenze budou odebrány. Před aktivací finanční dimenze můžete zadat hodnoty dimenze. Finanční dimenze lze však upotřebit až po aktivaci. Například nelze přidat finanční dimenzi do účetní struktury, dokud ji neaktivujete. Po kliknutí na možnost **Aktivovat** se všechny dimenze aktualizují a zobrazí se změny stavu. 

## <a name="translations"></a>Překlady

Na stránce **Překlad textu** můžete zadat text vybrané finanční dimenze v různých jazycích. Na stránce **Překlad hlavního účtu** můžete zadat text hlavního účtu v různých jazycích. 

## <a name="legal-entity-overrides"></a>Přepisy právnických osob

Ne všechny dimenze jsou u všech právnických osob platné. Některé dimenze kromě toho mohou platit jen v určitém období. V takových případech lze pomocí části **Přepisy právnických osob** určit společnosti, u kterých má být použití dimenze pozastaveno, kdo je vlastníkem a období aktivity dimenze.

## <a name="deleting-financial-dimensions"></a>Odstranění finančních dimenzí

V zájmu udržení referenční integrity dat lze finanční dimenze v řídkých případech odstranit. Při pokusu o odstranění finanční dimenze jsou vyhodnocena následující kritéria:

- Byla finanční dimenze použita pro zaúčtované a nezaúčtované transakce nebo jakýkoli typ kombinace hodnot dimenzí?
- Používá se finanční dimenze v nějaké aktivní účetní struktuře, struktuře rozšířeného pravidla nebo sadě finančních dimenzí?
- Je finanční dimenze součástí výchozího formátu integrace finanční dimenze?
- Byla finanční dimenze nastavena jako výchozí dimenze?

Pokud je odpověď na některou z těchto otázek kladná, finanční dimenzi nelze odstranit.

