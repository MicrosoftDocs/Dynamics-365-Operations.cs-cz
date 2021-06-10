---
title: Generování sestav v rámci zákona Affordable Care Act
description: Reporting zákona Affordable Care (ACA) generuje formuláře 1095-B a 1095-C podle části zákona Affordable Care **Mandát zaměstnavatele**.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1091460ee1996b944b760f3771007bd2a26666a9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053194"
---
# <a name="generate-aca-reports"></a>Generování ACA sestav

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Reporting zákona Affordable Care (ACA) generuje formuláře 1095-B a 1095-C podle části zákona Affordable Care **Mandát zaměstnavatele**.

> [!NOTE]
> Hlášení ACA je povoleno pouze pro právnické osoby ve Spojených státech.

## <a name="getting-started"></a>Začínáme

Chcete-li sledovat informace proformuláře 1095-B a 1095-C musíte nejprve vytvořit jednu nebo více skupin Affordable Care. Skupiny pokrytí Affordable Care označují:

- Nabídku pokrytí pro zaměstnance
- Podíl zaměstnance na nejnižší měsíční prémii, pokud je cena nad federální hranicí chudoby
- Program Safe Harbor, který využívá zaměstnavatel, je-li k dispozici

Skupiny pokrytí ACA, budete moci informace v těchto polích spravovat hromadně a nebudete muset upravovat každý záznam zaměstnance se stejnými podmínkami. Skupiny pokrytí ACA lze snadno přiřadit k jednomu nebo několika zaměstnancům pomocí funkce **Hromadné přiřazení** na stránce.

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a>Správa několika verzí skupiny pokrytí

Můžete spravovat několik verzí skupin pokrytí. Tato funkce vám umožňuje provádět změny, aniž byste museli vytvářet novou skupinu a znovu do ní přiřazovat zaměstnance. 

Poté, co vytvoříte skupiny pokrytí ACA, můžete hromadně přiřadit skupiny zaměstnancům s volbou **Hromadné přiřazení** volba. Můžete také jednotlivě označit, zda chcete sledovat a hlásit informace ACA, a přiřadit zaměstnance do skupiny pokrytí Affordable Care.

Nemusíte sledovat některé informace o pokrytí ACA, například u zaměstnanců na částečný úvazek. V tomto případě nastavte **Zpráva o pokrytí** pole na **Ne**. I když musíte každému zaměstnanci přiřadit sledovatelné informace ACA do skupiny pokrytí Affordable Care, můžete změnit následující možnosti pro měsíce s různými hodnotami:

- **Nabídka pokrytí**
- **Podíl zaměstnance na nákladech**
- **Institut "Safe Harbor"**

Chcete-li zadat výjimky z hodnot skupiny pokrytí ACA, vyberte **Pokrytí Affordable Care** na stránce **Podrobnosti pracovníka** (v části **Další informace** na kartě **Zaměstnání**).

## <a name="reporting-health-care-coverage"></a>Vykazování pokrytí zdravotní péče

Pokud zaměstnavatel nabízí sponzorované pokrytí s vlastním připojištěním a zaměstnanco tuto nabídku využívá (bez ohledu na to, zda pracuje na plný nebo částečný úvazek), je ve formuláři 1095-C nutné hlásit i další informace vedle údajů o tom, jaké (pokud nějaké) pokrytí zdravotního pojištění bylo nabídnuto zaměstnanci na plný úvazek. Ve výkazu musí být uvedeni všichni zaměstnanci (včetně závislých osob) krytí v rámci plánů zaměstnaneckých výhod sponzorovaných zaměstnavatelem, a to ve všech měsících, kdy pokrytí platilo. 

Zaškrtnutím políčka **Lze vykázat podle zákona ACA** můžete určit, zda je třeba daný plán zaměstnaneckých výhod vykazovat.

Pokud si zaměstnanci navíc zvolili i krytí závislých osob, je možné uvést data, kdy pokrytí začalo platit, na stránce **Udržovat výhody**. Chcete-li uvést, že se výhoda vztahuje na závislou osobu, vyberte tlačítko **Upravit** na panelu akcí na kartě **Rodinní příslušníci**.

Na stránce **Správce dat pokrytí rodinného příslušníka** můžete určit data pokrytí závislých osob v rámci zaměstnanecké výhody. Zadáním data na této stránce automaticky zaškrtnete políčko **Pokryto** na stránce **Udržovat výhody**.

## <a name="generate-1095-b-and-1095-c-forms"></a>Generujte formuláře 1095-B a 1095-C

Formuláře 1095-B and 1095-C můžete vygenerovat i v aplikaci a rozeslat je všem zaměstnancům. Systém může také elektronicky generovat formuláře 1095-C a přenosové soubory IRS 1094-C.  

Při generování formuláře 1095 C zadejte příslušný daňový rok a označte, zda mají být nahrazena čísla sociálního pojištění. Při tisku formulářů 1095-C pro více než 500 zaměstnanců obdržíte více než jeden soubor PDF. Doporučuje se zvýšit **maximální velikost souboru** v okně **parametry správy dokumentů** na 150 MB.

## <a name="viewing-information"></a>Zobrazení informací

Pomocí stránky **Pokrytí dostupné péče pro pracovníka** můžete zjistit, kteří zaměstnanci byli přiděleni k jednotlivým skupinám pokrytí, kteří zařazeni být nemusí a kteří přiřazeni nejsou.

U případných přepsaných výchozích hodnot skupiny pokrytí ACA se vedle změněné hodnoty zobrazí hvězdička. Pokud jsou hodnoty u všech 12 měsíců stejné a nebyly přepsány, hodnota bude uvedena ve sloupci **Všech 12 měsíců**.

Můžete také použít okno s dotazem, abyste pochopili, kteří zaměstnanci byli označeni jako zaměstnanci, kteří nejsou ACA vykazovatelní. Nemusíte sledovat, zda jim bylo nabídnuto pokrytí, a nebudete jim muset na konci roku vydat 1095-C. Vyberte **Nevykazovatelní v rámci ACA** v poli **Filtrovat podle** pro vygenerování seznamu všech zaměstnanců, kteří neobdrží 1095-C.

Kromě toho můžete také zobrazit všechny zaměstnance, kteří nejsou přiřazeni (pole **Vykazovat pokrytí ACA** je prázdné) nebo kteří byli přiřazeni do skupiny pokrytí ACA, jejíž platnost pro rok zadaný v poli **Rok** vypršela.

Seznamy zaměstnanců vygenerovaných podle zadaných filtrů je možné exportovat do aplikace Excel.

Pokud potřebujete hlásit kryté osoby, protože poskytujete pojištěné osoby, můžete zobrazit závislé osoby, na které se vztahují plány dávek, které jsou označeny jako **hlásitelné ACA**. V podokně akcí vyberte **Zobrazit data pokrytí rodinného příslušníka**.

> [!NOTE]
> Pouze plány dávek označené jako **hlásitelné ACA** zobrazit v okně dotazu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]